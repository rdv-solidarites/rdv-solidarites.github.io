---
layout: post
title: "Incident de production du 22 septembre 2021"
date: 2021-09-22
---

Le site a été très lent dans l’après-midi, puis inaccessible pendant environ 30 minutes, entre 16:00 et 16:26. Toutes les tentatives de connexion échouaient sur une erreur 500.

<!-- more -->

## Contexte

Nous avons des problèmes de performance depuis quelques semaines; globalement, pendant les heures de bureau, le temps d’accès au site augmente de façon significative. Nous avons activé l’« autoscale » des instances web chez notre hébergeur Scalingo en début de semaine. L’autoscale est configuré pour passer automatiquement de 2 à 5 instances web. Ce sont des instances L, avec un 1GB de mémoire. En pointe, ces instances consomment beaucoup, et atteignent rapidement la limite \(et donc swappent\). Nous étions depuis le début de la semaine en train de préparer des optimisations de performances.

## Chronologie
## Enseignements

    En fait, l’autoscale de Scalingo permet d’augmenter le nombre d’instances, mais pas d’augmenter la mémoire. Nous aurions pu commencer par passer sur des instances XL, ce que nous avons fait ensuite.

    Sur l’instance jobs, on a aussi un problème de mémoire, mais c’est moins critique. Il y a a priori une fuite de mémoire, mais la seule conséquence est que l’instance est redémarrée quand elle atteint la limite, et reprend les jobs là où elle s’est arrêtée.

    La base de données PostgreSQL est actuellement limitée à 30 connections. Nos instances web font tourner Puma avec 5 threads; avec 5 instances web et l’instance jobs, on atteind la limite!

## Analyse

* Le passage a 5 instances L a permis de mitiger les problèmes, mais ne règle rien: notre problème est plus un problème d’utilisation mémoire que de processeur.
* Le passage à 5 instances XL a permis de passer la journée de jeudi sans tomber à nouveau.
* Le déploiement des optimisations vendredi après-midi a fait chuter le temps de réponse médian, qui reste autour de 150ms, alors qu’il était autour de 2-3 secondes.

![Temps de r&#xE9;ponse mercredi, jeudi et vendredi. Le trait rouge indique le d&#xE9;ploiement des optimisations.](../../.gitbook/assets/image.png)

## Travaux restants

* Le serveur de base de données est lui aussi sous-dimensionné: il atteind ses limites de mémoire.
* * Nous avons un serveur avec 512Mo; nous pouvons passer soit à un serveur 1Go, soit à un cluster de 2 nodes avec chacun 512Mo. Cette deuxième solution a aussi l’avantage de permettre des montées de version de la base de données sans interruption de service.
  * Nous avons commencé la procédure mais rencontrons là aussi des erreurs côté scalingo. 
* La charge CPU reste assez élevée sur les 3 instances XL. On pourrait peut-être mieux servis par une ou deux instances 2XL. 

