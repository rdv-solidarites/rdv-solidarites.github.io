---
layout: post
title: "Réunion référente"
date: 2021-08-10
---

## Démo

* [Focus sur le champ de recherche #1595](https://github.com/betagouv/rdv-solidarites.fr/issues/1595)
* [ Ajouter les dates de naissance et age dans les listes déroulantes de sélection d'usager #1603 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1603)
* [La modificaiton d'un usager depuis le tunnel de prise de rendez-vous crée un doublon #1606 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1606)
* [Impossible de supprimer un usager proche #1605 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1605)
* [ Connecteur pour le 77 #1599 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1599)
* [ Zone de recherche pas accessible dans la liste des responsables #1604 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1604)


## Connecteurs pour l'envoie de SMS

Travaux en cours pour le 92. Connecteur pour le 77 normalement opérationnel. Nous attendons la disponibilité de la DSI pour pouvoir faire la transition. Il vaut mieux qu'il y ait des personnes disponibles pour surveiller que tout fonctionne bien.

## Liste usager

Lorsqu'un usager n'a pas de date de naissance, nous n'affichons rien. Il serait préférable d'afficher l'information que nous n'avons rien.

Il y a aussi [une discussion sur le fait de rendre la date de naissance obligatoire](https://forum.rdv-solidarites.fr/t/rendre-obligatoire-la-date-de-naissance/67).

Les deux ne sont pas incompatible. Il y aura, pendant un moment, les anciens comptes.

[Ticket 1621 à propos de l'ajout de l'information « pas de date de naissance »](https://github.com/betagouv/rdv-solidarites.fr/issues/1621)

## Référent usager

Pour l'ajout de référent à un usager, nous affichons la liste de tous les agents. C'est long et pas simple à manipuler. Il serait bien d'ajouter un champ de recherche (un peu comme sur la page qui liste les agents)

[Ajouter un champ de recherche agent dans la page des référents #1622](https://github.com/betagouv/rdv-solidarites.fr/issues/1622)

## Base de développement

Note pour l'équipe de développement.

Nous utilisons un fichier qui charge des données exemples pour avoir une base de développement opérationnelle. Le problème c'est qu'elle ne représente pas très bien la réalité. Il n'y a pas assez d'usagers et d'agents.

Il serait intéressant d'augmenter le nombre d'agents et d'usagers dans ce fichier.

[Augmenter le nombre d'usager et d'agent dans le fichier de construction #1623](https://github.com/betagouv/rdv-solidarites.fr/issues/1623)


## Tableau des Prio

Le ticket sur [Préciser qui est à l'initiative de l'annulation du rendez-vous #1551](https://github.com/betagouv/rdv-solidarites.fr/issues/1551) est en cours. Il a donc été retiré du tableau. **Les points qui avaient été attribués à ce tickets par les territories sont à nouveau disponible**

Actuellement, le sujet qui ressort comme prioritaire de ce tableau concerne un bug. [Afficher l’alerte de numéro de téléphone existant aussi quand on crée un usager Responsable #1509](https://github.com/betagouv/rdv-solidarites.fr/issues/1509). Il manque un « warning » sur les doublons de numéro de téléphone dans l'application.

Un nouveau ticket à été ajouté dans le tableau : [
Débrayer l’envoi de notification au rendez-vous #1617 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1617)

## Statistique

Dans le cadre du ticket [[stats][departement] exporter des statistiques par département #1077](https://github.com/betagouv/rdv-solidarites.fr/issues/1077) nous poussons un peu plus l'usage de [Metabase](https://www.metabase.com/). C'est un outil que nous avons installé sur une instance à coté de RDV-Solidarités. Branché en lecture seul sur la base de production. Cet outil nous permet d'écrire des requêtes assez simplement pour faire des tableaux, courbes, diagrammes, le tout exportable.

Une première étape à été mise en place avec un tableau d'export des rendez-vous du mois précédent pour chaque département.

Il reste à inviter les agents référentes à se créer un compte pour accéder aux divers diagramme.


Il y a également un email de rappl à faire aux référentes pour évoquer les rendez-vous qui ont une date très éloigné dans le futur et la liste des agents ayant une adresse @gmail.com

## Relation ANCT

Il a été abordé la question de la relation avec l'ANCT. Maintenant que la convention est signées par la plupart des départements, est-ce que l'ANCT compte avoir un échange avec les département ?

- Un Copil est prévu le 23 septembre 2021
- Comment l'ANCT va travailler avec les départements, une feuille de route ?
- Est-ce qu'il y a un référent à l'ANCT ?
- Avoir un point financier ? (prévu au copil)
- parler de 2023 (l'après convention actuel)