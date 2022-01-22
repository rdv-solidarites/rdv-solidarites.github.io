---
layout: post
title: "Réunion référente"
date: 2021-08-24
---

## Démo

* [Disparition des fonds de couleur dans les statistiques](https://github.com/betagouv/rdv-solidarites.fr/issues/1650)
* [Limiter la pose de rendez-vous dans le futur](https://github.com/betagouv/rdv-solidarites.fr/issues/1600)
* [Afficher correctement les absences récurrentes dans l’onglet “En cours”](https://github.com/betagouv/rdv-solidarites.fr/issues/1613)
* [Préciser qui est à l'initiative de l'annulation du rendez-vous](https://github.com/betagouv/rdv-solidarites.fr/issues/1551)
* [Ajouter un connecteur pour SFR (92)](https://github.com/betagouv/rdv-solidarites.fr/issues/1589)

## Message d'erreur

Lorsque le champ date d'un rendez-vous est en dehors de la fourchette normale, le message contient l'attribut en anglais. C'est peut clair pour les agents.

https://github.com/betagouv/rdv-solidarites.fr/issues/1659

## Rendez-vous en doublon

À propos du ticket : https://github.com/betagouv/rdv-solidarites.fr/issues/1633

Nous évoquons le fait de faire en sorte qu'au moment d'ajouter un collègue sur un rendez-vous, nous prenions également en compte son agenda.

## Point sur Metabase et les statistiques

Les invitations ne semblent pas avoir été reçu. Aucune n'a été relancé pour le moment. Les référentes se demandent si elles doivent créer un compte ou pas.

L'équipe se pose des questions sur la pertinence d'utiliser métabase. Les questions de RGPD et de finalité posent des questions. **Peut-être que nous n'avons pas besoin de metabase ?**

Pourquoi nous cherchons une solution : 
- Certains départements aimeraient faire plus de statistiques
- Les données sont toutes dans une même base pour tous les départements
- Il n'y a pas d'export anonymisé pour le moment
- Pour la finalité statistique, l'export par organisation est pénible
- Pour la finalité accueil, l'export par organisation bien, voir trop gros


## Mise en production

Aujourd'hui, l'équipe met en production dès quelle a fini quelque chose. Cela pose divers problèmes sur le terrain.

Il serait intéressant de permettre aux référentes d'être informé en avance des mises en production pour des enjeux :
- technique vis-à-vis des connecteurs / DSI
- usage vis-à-vis des utilisateurs

Difficile pour les référentes d'être prise à partie au moment des remontés utilisateurs. Parfois positif, et là ça convient, et parfois négatif, c'est plus délicat. Surtout qu'il est difficile de venir en aide aux agents alors que l'on n’est pas au courant de la fonctionnalité livrée.

Pas de mode de communication mise en place pour suivre des mises en production aussi fréquente.
Dans les modes d'organisation alternatifs mis en place actuellement, nous avons : 
- Amandine (77) improvise une newsletter hebdo
- Élodie (62) fait 3 visio par an
- Clarisse (92) la page d'accueil peut service de zone d'information

_Et comment ça peut se passer pour les personnes qui partent en congés ?_

Ce qui serait intéressant, c’est 
- Avoir un temps de test et de surtout de prise de connaissance avant de livrer en production.
- Pouvoir anticiper les changements avec une communication adaptée en fonction des départements et des agents
- Attention à ne pas trop ralentir non plus, ça serait dommage.
- Avoir une page d'accueil dans l'application pour pouvoir passer des messages, notamment sur les mises en production