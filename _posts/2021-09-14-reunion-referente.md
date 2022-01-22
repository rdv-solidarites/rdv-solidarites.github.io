---
layout: post
title: "Réunion référente"
date: 2021-09-14
---

## Recette

- [ [Home] Affiche les services disponible #1701 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1701)
- [ Ne pas afficher le prénom des agents dans les notifications aux usagers #1697 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1697)
- [ Faire un connecteur SMS pour la Somme (80) #1664 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1664)

**Sans notification particulière, ces tickets seront mis en production jeudi prochain, à partir de 12 h.**

## Démo et Recette

Pour pouvoir utiliser l'environnement de recette, dans l'état actuel, les référentes ont besoin de connaître les usagers, les agents et leur service pour pouvoir se connecter (email et mot de passe). Une petite page de documentation pourrait sans doute convenir dans un premier temps.

https://doc.rdv-solidarites.fr/communaute-and-gouvernance/environnement-de-recette

Les données disponibles actuellement, les mêmes que l'environnement de développement, ne sont pas représentative de ce qu'il se passe en production.

Il serait intéressant de pouvoir extraire et anonymiser une partie (petite) des données de production pour avoir un jeu de données représentatif.

Une autre option serait de copier le contenu de la base de démo en recette. Ça permettrait aux référentes de ne pas avoir à tout refaire.

À propos de l'environnement de démo, il y a besoin de copier les libellés de motifs qui sont en production sur l'environnement de démo (et donc de recette ?)

Il serait également intéressant de pouvoir copier tout ou partie de la configuration (sectorisation, motif, agent ?) de la production sur l'environnement de démo. Sans les usagers, les RDV, et peut-être même sans les agents et leurs éléments d'agenda.

> Est-ce que la recette pourrait être un environnement pour les départements déjà au consortium ? Avec des données copié depuis leur environnement de production.
> Alors que la démo serait pour les départements intéressé par RDV ? Nous pourrions le remettre à zéro régulièrement.
>
> Non, pas forcement. L'environnement de recette est en avance par rapport à la production. Ce n'est pas forcement le bon environnement pour faire des formations.
> Par contre, il serait intéressant de faire en sorte que la base de démo et de recette soit la même (dans le sens, copier la démo sur la recette)
> Il resterais à copier la configuration de production sur la démo.
> -- Yannick

## Nouveauté API et connecteurs SMS

L'équipe doit informer le Pas-de-Calais (62) et la Drôme (26) des modifications qui ont eu lieu dans l'API à propos des status de rendez-vous.

L'équipe doit prendre rendez-vous pour tester la configuration d'envoi de SMS avec :
- la Somme (Fabienne & Sandra ?)
- la Seine-et-Marne 
- les Hauts-de-Seine

> Surprise sur le volume et le budget que ça représente. Une notification correspond à 2 sms (taille du message).
> -- Élodie (62)

Il faut compter en général deux notifications par RDV. Chaque notification envoie un message trop long pour un seul SMS. C'est donc deux SMS qui sont envoyé à chaque notification. **Cela fait un total de quatre SMS envoyés par RDV**

https://doc.rdv-solidarites.fr/technique/envoie-de-sms

À noter qu'il y a un premier ticket à propos du suivi des notifications. Il permettra de poser une première étape sur le sujet : https://github.com/betagouv/rdv-solidarites.fr/issues/1431

## Documentation

Léry, un membre de beta.gouv.fr très actif sur les aspects documentaire, a fait un « audit » de notre doc et nous propose des actions.

> Serait-il possible de ne pas afficher la lister des sujets / pages sous chaque catégorie ? Cela pourrait faire une liste trop grande !
> 
> -- Christelle (64)

_Vis-à-vis de la page https://doc.incubateur.net/template-de-doc/_

## Statistique

Nous avons parlé des statistiques et du besoin d'avoir un fichier consolidé à partir de l'interface de territoire.

https://github.com/betagouv/rdv-solidarites.fr/issues/1719

## Traçabilité usager

Nous avons évoqué l'intérêt pour le ticket [Traçabilité de la fiche usager #1675](https://github.com/betagouv/rdv-solidarites.fr/issues/1675)

Nous avons également précisé qu'il est nécessaire de laisser un accès à l'historique d'un rendez-vous tous les agents pouvant le voir (et pas uniquement aux admins)

## Libellés de motif

Nous avons reparlé de laisser les agents admin créer des libellés comme ils le souhaitent. Référence à l'échange sur le forum https://forum.rdv-solidarites.fr/t/creer-un-motif-et-son-libelle-sans-lequipe-technique/138.

C'est toujours un sujet de discussion et non un ticket à prioriser. Est-ce que c'est un ticket à prioriser à bien à prendre dans le flux normal ?

## Performances

> J'ai remarqué des lenteurs autour de 14h sur RDV-Solidarités.
> -- Élodie

Nous pourrions faire un travail de fonds pour améliorer les performances. Il y a de quoi faire.

Nous pourrions aussi ajouter une instance (voir mettre en place le système de Scalingo automatique proposé par Scalingo ?) pour répondre à ce problème de performance.

## Data.insertion - RSA

L'utilisation de Data.insertion (RDV-insertion ?) pas de surcout pour les départements déjà au consortium.

Pour en savoir plus sur le projet https://beta.gouv.fr/startups/data.insertion.html

Attention, dans certains départements, l'équipe chargée de l'insertion n'est pas la même que celle chargée du médico-social. Nous pouvons peut-être aider à faire le lien entre les deux équipes utilisatrice de RDV-Solidarités.

L'équipe de RDV-Solidarités, avec la présence ou non d'un membre de Data.insertion, pourrait communiquer sur les travaux de Data.insertion dans RDV-Solidarités quand il y en a. Ça permettrait aux référentes d'être au courant.

## Protocole de la réunion référente

Nous avons évoqué le fait d'envoyer le compte rendu de cette réunion (et des suivantes) par email, en plus de la placer sur le forum.

J'en ai profité pour mettre à jour la documentation des rituels de l'équipe https://app.gitbook.com/@rdv-solidarites/s/rdv-solidarites/communaute-and-gouvernance/rituels