---
layout: post
title: "Réunion référente"
date: 2021-08-17
---

## Démo 

- Statistiques par département (metabase)
- Préciser qui est à l'initiative de l'annulation du rendez-vous​
- L'annulation par l'administration ne libère pas le créneau

## Présentation des changements de bouton d'état de RDV

Questionnement sur la phrase « Annulé pour raison administrative ». C'est un terme qui peut prêter à confusion. À l'initiative de la collectivité ? Du Service ?

« La raison administrative » n'est pas dans le vocabulaire.

Une meilleure option trouvée pendant la réunion semble être :

> Annuler à l'initiative du service


## Affichage de rendez-vous dans l'agenda

Afficher ou pas les rendez-vous annuler ?

Certains agents semblent vouloir supprimer les rendez-vous pour ne plus les voir apparaître dans l'agenda.

Une solution serait de ne pas les afficher dans l'agenda. Ceci étant, pour d'autres agents, c'est rassurant de voir que le rendez-vous n'a pas disparu, mais qu'il a été annulé. C'est parfois pratique lorsque c'est l'usager qui le fait de son côté.

Il ne semble pas y avoir une bonne solution pour toutes. Peut-être qu'à long terme, nous pourrions ne pas les afficher. 

En attendant, nous allons revoir le filtre actuellement présent sur l'agenda. Il est censé filtrer les rendez-vous affichés en fonction de leur statut. Nous allons l'enlever et mettre une case à cocher pour afficher ou pas les rendez-vous annulés.

https://github.com/betagouv/rdv-solidarites.fr/issues/1634

## Planning pour les personnes chargées d'accueil

Un sujet déjà évoqué sur le forum [Un seul écran l’agenda de tous les professionnels présents un même jour dans la structure](https://forum.rdv-solidarites.fr/t/un-seul-ecran-l-agenda-de-tous-les-professionnels-presents-un-meme-jour-dans-la-structure/139) refait surface.

Ça devient un besoin récurrent : pouvoir visualiser la journée de travail sur une seule page. C'est très utile pour les agents chargés de l'accueil qui ont une idée de l'organisation de la journée d'un seul coup d'œil.

Élise (14) avait fait remonter ce genre de demande (avec un document Excel joint pour avoir une idée de la visualisation). Vaéa (77) semblait également intéressé (via le forum).

Ce matin, c'est Magalie (22) qui nous a fait remonter ce besoin. Elle nous a également envoyé un tableau Excel aujourd'hui utilisé par les personnes chargées d'accueil des Côtes d'Armor.


## Ajout d'un référent

L'ajout de référent est parfois pénible. Dans la page, il peut y avoir des dizaines et des dizaines d'agents. Une zone de recherche / filtre serait bien pratique.

Nous en avions parlé lors d'[une précédente réunion](https://forum.rdv-solidarites.fr/t/reunion-referentes-du-10-aout-2021/282/2#rfrent-usager-4), je n'avais pas retrouvé le ticket, mais il est bien là https://github.com/betagouv/rdv-solidarites.fr/issues/1622


## Précision sur certains tickets du tableau des prios

Il y avait 3 tickets en questionnement, nous les avons abordé. Certains éléments de nos discussions sont maintenant dans le ticket pour essayer de le rendre plus clair.

- [Revoir la façon de saisir une heure](https://github.com/betagouv/rdv-solidarites.fr/issues/1245)
- [Configurer les notifications de plages d'ouvertures et d'absences comme pour les RDV](https://github.com/betagouv/rdv-solidarites.fr/issues/1490)
- [ Afficher l’alerte de numéro de téléphone existant aussi quand on crée un usager Responsable](https://github.com/betagouv/rdv-solidarites.fr/issues/1509)


## Lien pour une visio dans un rendez-vous

Élodie (62) à remonté le besoin de pouvoir ajouter un lien vers un outil de visio (vers une salle) pour les rendez-vous « en ligne ». De plus en plus répandu.

Après avoir rapidement écarté l'ajout d'une zone libre pour ajouter des infos dans les notifications (trop de risque RGPD), nous avons fini par fait le lien (merci Sandra) avec le fait que la visio est un lieu.

Clarisse (92) a déjà effectuée une demande qui pourrait répondre à ce besoin aussi : l'[ajout d'un lieu tiers pour un RDV](https://forum.rdv-solidarites.fr/t/lieux-tiers-pour-des-rdv/275)

L'idée serait, dans le tunnel de prise de rendez-vous et dans la fiche d'un rendez-vous, de pouvoir, au moment du choix du lieu, préciser « autre lieu », et ainsi d'avoir une zone de saisie libre.

Cette zone de saisie serait contrôle malgré tout pour vérifier qu'elle contient une adresse (BAN) ou bien une URL vers un système de visioconférence.

https://github.com/betagouv/rdv-solidarites.fr/issues/1639


## Tunnel de prise de rendez-vous, étape 4, vérifications

Lors de la dernière étape de la prise de rendez-vous, l'agent fait parfois une dernière vérification sur le numéro de téléphone vers lequel va être envoyé le SMS (ou le mail). Si ce n'est pas le bon, l'agent à tendance à cliquer sur le nom de la personne affiché au-dessus du numéro de téléphone. Cela nous amène vers la fiche usager, sans possibilité de revenir dans le tunnel de prise de rendez-vous. Tout est à refaire...

Le lien vers l'usager dans la zone 4 du tunnel de prise de rendez-vous pourrait ne pas perdre le contexte

https://github.com/betagouv/rdv-solidarites.fr/issues/1637


## Le nom de la commune et plus parlant que le code postal

Dans les exports (metabase et rdv-Solidarités), il faudrait avoir systématiquement le nom de la commune (et pourquoi pas laisser le code postal). Ça serait plus simple pour effectuer des tris. Certains codes postaux comptent plusieurs communes.

https://github.com/betagouv/rdv-solidarites.fr/issues/1638


Nous avons également parlé de problématique autour du RGPD et des exports de données. Peut-être que ce n'est pas une si bonne idée d'utiliser metabase ? Un sujet à rediscuter sans doute.


## Ajout dans le tableau de priorisation

Suite à cette réunion, nous avons ajouté 3 nouvelles entrées dans le tableau des priorisations.