---
layout: post
title: "Réunion référente"
date: 2021-09-07
---

## Démo

_Des éléments techniques uniquement, aucune démonstration_

## COPIL / Comité stratégique

Un point sur le déploiement et les difficultés de chaque département sera fait au COPIL. Nous avons besoin de recueillir des retours (quantitatif et qualitatif) des acteurs et actrices RDV-Solidarités des départements.

La présentation sera envoyé sous peu pour relecture et surtout pour récolter les retours évoqué ci-dessus.

## Conventions

Après un retard de signature de convention coté ANCT (principalement dû aux congés d'été), certaines conventions ont été envoyées vers les départements.


## Mise en production

Nous allons essayé une autre façon de procéder. La page [flux de production](https://doc.rdv-solidarites.fr/communaute-and-gouvernance/flux-de-production) de la doc documente le nouveau processus.

En résumé, nous allons ajouter une étape « recette » avec un environnement correspondant à partir duquel nous ferons les démonstrations le mardi. Si tout le monde est d'accord, le jeudi, nous basculerons ces modifications en production.

Dans certains cas, vous aurez peut-être besoin de plus de temps pour communiquer aux agents. Nous pourrons toujours retarder la mise en production à la demande.

De la même manière, nous avons aussi défini un mode de livraison plus rapide pour pouvoir corriger des bugs ou bien suivre une procédure particulière dans des cas exceptionnels.


## Outils de discussion pour l'équipe et les personnes référentes

Proposition d'expérimentation d'une liste de diffusion. Une adresse email permettant d'envoyer un email à toutes les personnes référentes ainsi qu'à l'équipe.

> - Retour en arrière ? 
> - Le forum est peut-être plus facile pour organiser, suivre, participer.
> - Ajouter des éléments dans la boite mail ajouter une charge mentale qui peut être aussi pénible.
> - Le forum permet de centraliser les sujets, dans la boite mail ça va être plus difficile.

Dans les échanges, nous notons que le 92, 77, 62 sont pour conserver le forum plutôt que la liste de diffusion.

> je ne vais pas souvent sur le forum. Fabienne est plus en observation sur le forum, mais pas de participation. La réunion référente et les ateliers spécifiques sont plus simple pour parler d'un sujet.
> -- 80 (Sandra)

Le forum permet d'avoir une visibilité plus simple des sujets importants pour les autres départements.

Il y a des discussions qui commencent mais qui ne finisse pas (n'avance pas). C'est frustrant. Est-ce que c'est le support qui crée ça ou simplement le fait qu'il manque une modération ?

Le fait d'avoir des discussions orale permet d'avancer plus que l'écriture...

_Est-ce que nous abandonnons l'expérimentation ?_

**À noter que le Le forum est toujours innacessible dans les Côtes d'Armor.**

## Documentation

> Où est le guide PDF ? Est-il mis à jour quelque part ? Il contient les principales étapes de prise en main de l'outil.
> -- Magalie (22)


Ce guide est un export PDF de la page tutoriel (?) https://app.gitbook.com/@rdv-solidarites/s/rdv-solidarites/tutoriels/tutoriel qu'avait réalisé Camille.

La documentation doit évoluer. Il faudrait envisager une entrée agent et une pour les admins (une aussi pour la DSI ? une pour les référentes pour évoquer le mode de fonctoinnement de l'équipe ? Une pour l'équipe). Lerry de beta.gouv.fr va nous aider.

Trois ticket ont été créés pour mettre à jour la documentation.
- [Mettre à jour le tutoriel d'utilisation #1691](https://github.com/betagouv/rdv-solidarites.fr/issues/1691)
- [Mettre à jour le tutoriel de paramétrage d'une organisation #1689](https://github.com/betagouv/rdv-solidarites.fr/issues/1689)
- [Mettre à jour le tutoriel de paramétrage d'un territoire #1690](https://github.com/betagouv/rdv-solidarites.fr/issues/1690)

Reste à voir comment communiquer les versions PDF de ces pages. Un lien depuis le service ?


## Droits d'accès agenda

Avoir un agenda par agent, et gérer les accès lecture/écriture par agents. Nous avons amorcé un ticket sur le sujet https://github.com/betagouv/rdv-solidarites.fr/issues/1692. Dès qu'il est terminé, il fera sont entrée dans le tableau de priorisation.

## Clôture du ticket sur l'alerte de doublons

Nous avons décidé de clôturer le ticket [Afficher l’alerte de numéro de téléphone existant aussi quand on crée un usager Responsable #1509](https://github.com/betagouv/rdv-solidarites.fr/issues/1509).

Le coût de correction de ce problème en temps de réalisation et en complexité ajouté au code source RDV-Solidarités est élevé.

Sachant que 
- nous allons devoir modifier intégralement ces parties
- le doublon est détecté malgré tout, mais a postériori
- le cas d'usage est rare (?)
- le doublon sur le téléphone n'est pas bloquant

Nous pensons qu'il est préférable de fermer le ticket et de passer à autre chose.