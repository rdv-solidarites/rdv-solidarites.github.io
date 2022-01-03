---
layout: post
title: "Réunion référente du mardi 13 avril 2021"
date: 2021-04-13
---

## Démo

Les nouveautés de la plateforme depuis le 30 mars 2021.

- [Empêcher d’inviter des agents aux autres organisations](https://github.com/betagouv/rdv-solidarites.fr/issues/1308)
- [Ajouter des validations de présence sur le nom et prénom des agents](https://github.com/betagouv/rdv-solidarites.fr/issues/1268)
- [harmoniser les icônes d'actions du tableau admin/agents#index](https://github.com/betagouv/rdv-solidarites.fr/issues/1267)
- [fix bug when rendering rdv_upcoming_reminder mail](https://github.com/betagouv/rdv-solidarites.fr/issues/1318)

- [Mentionne le niveau d'accessibilité dans le bas de page](https://github.com/betagouv/rdv-solidarites.fr/issues/1265)
- [Rendre le statut « vu » accessible une heure avant le RDV](https://github.com/betagouv/rdv-solidarites.fr/issues/1263)
- [Ajouter un numéro de téléphone pour les lieux](https://github.com/betagouv/rdv-solidarites.fr/issues/1146)
- [dans le tunnel de prise de rendez-vous, l'étape 3 apparait en doublon dans le bas de page](https://github.com/betagouv/rdv-solidarites.fr/issues/1289)
- [Amélioration du tableau des motifs](https://github.com/betagouv/rdv-solidarites.fr/issues/1174)

## Développement en cours

Les tickets en cours  de réalisation ou de test au 13 avril 2021 :
- [Agenda agents inter-organisations](https://github.com/betagouv/rdv-solidarites.fr/issues/1185)
- [Améliorer l'affichage des messages d'info et d'alerte dans l'interface usager](https://github.com/betagouv/rdv-solidarites.fr/issues/1305)
- [API invitation usager](https://github.com/betagouv/rdv-solidarites.fr/issues/1046)
- [nettoyage de messages d'alerte](https://github.com/betagouv/rdv-solidarites.fr/issues/1214)
- [Affecter un agent à plusieurs services](https://github.com/betagouv/rdv-solidarites.fr/issues/1300)
- [réparer réconciliation sur email pour FranceConnect](https://github.com/betagouv/rdv-solidarites.fr/issues/1237)
- [corriger ICS suppression plage ouverture pour outlook](https://github.com/betagouv/rdv-solidarites.fr/issues/1275)

_Liste sur le [tableau de développement](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true)_.

## Priorisation

À ce jour, un ticket [S] est traité en moyenne en 1 journée, [M] est traité en 8 jours, [L] en 18.

- [S] dans le tunnel de prise de rendez-vous, la vérification de présence du numéro de tel à l'air cassée pour les usagers proches
- [S] UI des alertes dans le tunnel de rdv admin étape 3
- [M] Améliorer l'affichage des messages d'info et d'alerte dans l'interface usager
- [L] L Permettre l'envoie d'un email avec ICS pour l'agent à chaque RDV (paramétrable au niveau d'une orga ou d'un département)
- [M] Envoyer des notifications mails avec fichier ICS aux agents pour les absences (faire comme pour les plages d'ouverture)
- [S] Réduire la liste de motif dans le formulaire de plage d'ouverture avec un filtre par service
- [M] Regrouper suppression et annulation RDV dans un bouton
- [S] Filtre les absences passées
- [M] Inclure la commune de l'usager responsable dans l'export
- [S] Investiguer pourquoi le bouton "prochain créneau" n'apparait pas toujours (bug)

Il ressort de la conversation :
- l'envie d'avoir un protocole presque automatique de priorisation
- le fait que ce protocole serait trop complexe, et nous empêcherais de faire autrement parfois
- Avoir l'information sur le poids / durées estimée est important pour prioriser
-

## Convention

Suite au mail de relance, où en sommes nous des signatures de la nouvelle convention.

Point à peine abordé faute d'information.

## Discussion libre

### UX des motifs

Nous avons reparlé des problèmes d'UX en général : comment avoir un budget pour embaucher une personne à ce poste ?
Et en particulier pour traiter le problème de choix de motifs (pour les départements/services qui en ont beaucoup)


### Quelques points soulevé durant la réunion

**Prénom et nom des agents**

Quand il ne manque qu'un des deux (prénom/nom) aucun n'apparait dans le tableau. Ce cas ne pourra plus se produire. Il serait peut-être intéressant de lister les agents dans ce genre de situation et de leur envoyer un message pour leur demander de procéder à une correction.

**Notification SMS avec numéro de téléphone**

Maintenant que les lieux ont des numéros de téléphone, il serait judicieux d'utiliser ce numéro dans les notifications SMS à la place du numéro d'organisation.

_En question bonus : pourquoi garder des numéros de téléphone sur les organisations ?_

**Demande de fonctionnalité de duplication des absences**

Au moment de parler des priorités, il a été demandé à ce que les absences puissent être dupliquée. Ça semble plus important que le fait d'avoir un onglet avec les absences passées.

> > En question bonus : pourquoi garder des numéros de téléphone sur les organisations ?
>
> Pour les organisations qui ne font pas d'accueil téléphonique sur les lieux de RDV.
> Si il n'y a pas de numéro de téléphone renseigné sur un lieu de RDV, par défaut la machine doit inscrire le numéro de l'organisation dans les notifications.
>
> -- Élodie (62)


> Je pense que dupliquer une absence et les classer sont deux choses différentes.
> Le fait de les classer lorsqu'elles sont passées semble cohérent si on compare avec le visuel des plages d'ouverture.
> Plutôt que de s'ajouter des questions supplémentaires, ne peut-on pas trancher cette question en se disant quel argument s'oppose à la création de cet onglet des absences passées ? :wink:
> Merci @Yannick
>
> -- Sandra (80)
