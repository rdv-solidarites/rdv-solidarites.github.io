---
layout: post
title: Réunion référentes du 20 juillet 2021
date: 2021-07-20
---

## Démo

- [ Création et suppression d'absence sans titre #1574 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1574)
- [ Réduire l'usage de la suppression de RDV #1043 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1043)
- [ Mettre en place un connecteur pour le fournisseur de SMS Contact Expérience #1571 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1571)
- [ Rechercher un usager sans voir la liste complète #1348 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1348)
- [ Ne pas afficher le nom et prénom de l'usager dans le fichier ICS #1587 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1587)

## Annulation de rendez-vous

La démonstration à propos du lien de suppression d'un rendez-vous, accessible uniquement aux profils admin maintenant, amène la question autour de « qui à annulé un rendez-vous ». C'est le ticket le plus priorisé du tableau :)

https://github.com/betagouv/rdv-solidarites.fr/issues/1551

## Historique des rendez-vous

> Qui supprime les rendez-vous ? Le département ? Les admins ? L'équipe RDV-Soldiarités ? Selon quelle règle ?

Il y a plusieurs sujets :
- l'historique des rendez-vous
- les comptes usagers
- le reste (agents, motifs, lieux, ...)

Le sujet le plus important est sur l'historique des rendez-vous. Ce sont eux qui sont porteur de données de santés. Ensuite viendra le temps des comptes usagers, porteurs de données personnelles sensible (adresse, email, téléphone)

Si on supprime réellement un rendez-vous, on supprime aussi l'historique statistique. Nous pouvons rendre un rendez-vous anonyme. Supprimer l'usager, ne garder que sa commune dans le rendez-vous. Idem pour les lieux de rendez-vous sur des motifs « à domicile », ne garder que la commune.

Se posera la question technique sur le lieu de stockage des RDV. Il serait intéressant de déplacer les rendez-vous historique, dans une table dédiée pour les statistiques uniquement.

Nous pourrions aussi calculer les statistiques et supprimer les rendez-vous.
Cette option permet de ne stocker que ce dont nous avons l'usager. Par contre, elle empêche tout « nouveau » calcul. Si une nouvelle statistique viens à être demandé, elle ne pourra pas être calculé sur l'historique (puisque les informations ne seront plus là).


Assez proche de ce sujet il y a également la question des départements sans outil de suivi pour les PMIs. Est-ce qu'ils utilisent RDV comme outil de suivi ? Si oui, comment faire la transition ?


> Que deviennent les données supprimer ?
> -- Question des DPOs du 64.

Elles disparaissent, ne sont plus accessible, pour personne.

**Attention au impact sur les autres systèmes interconnectés !**


## Filtre usager

> Serait-il possible d'ajouter la date de naissance dans les critères de recherche ?


## Nom de l'usager dans le fichier ICS

Dans le résumé du rendez-vous, envoyé dans le fichier ICS, il y a le nom et prénom de l'usager. Avant, les ICS ne fonctionnaient pas bien sur la synchro par email. Maintenant oui, et la présence de cette information est génante.

Les agendas Outlook et Zimbra sont souvent partagés entre collègues d'un même département. Pour celles qui ne souhaitent pas partager les informations sensible sur les rendez-vous d'un service ou d'un autre, il ne faut pas afficher ces informations personnelles.

Ancien résumé dans fichier ICS (notification mail pour synchronisation Outlook & autres)
- "RDV Patricia DUROY <> Consultation Prénatale"

Après correction
- "RDV Consultation Prénatale"

Ajout possible (url vers la fiche RDV de RDV-Soldiarités):
- "RDV Consultation Prénatale http://localhost:5000/admin/organisations/1/rdvs/4?agent_id=2"
Voir [Rajouter des liens vers RDV-Solidarités dans les fichiers ICS envoyés aux agents](https://forum.rdv-solidarites.fr/t/rajouter-des-liens-vers-rdv-solidarites-dans-les-fichiers-ics-envoyes-aux-agents/213)

Il sera peut-être nécessaire d'ajouter de la configuration en proposant chaque éléments.

## Configurer les champs utiliser dans une fiche usager (64)

Il y a beaucoup de champs inutilisé dans les fiches usagers. Certains départements souhaiteraient ne pas les voir afficher !

Faire une analyse de l'utilisation en production des champs
- Notes
- Caisse d'affiliation, Numéro d'allocataire, Situation familiale, Nombre d'enfants, Logement

Le mieux serait de supprimer ces champs.
À voir selon l'usage.

Je note que aucun département présent aujourd'hui utilise ces champs sociaux.
- nombre d'enfants et situation familiale dans le 80, mais ça ne devrait pas.
- numéro d'allocataire pour le RSA dans le 77 (voir Data.insertion)

## Préciser un peu le ticket sur les préférences de notifications

https://github.com/betagouv/rdv-solidarites.fr/issues/1490

Nous avons précisé durant la réunion.
L'idée est de permettre aux agents de choisir de recevoir ou pas les notifications email à propos de la création, modification, suppression de leurs plages d'ouvertures et absences.

## Sujet à ajouter

dans le forum et surtout dans le tableau
> Autres propositions en attente :
> - Décocher l'envoi de SMS et/ou mail à la prise de rendez-vous
> - Décocher la confirmation à la prise de rendez-vous et n'envoyer que le rappel 48h avant
> - Décloisonner les services

- Pouvoir lié plusieurs personne à une autre (Proche vs Responsable)
- Date de naissance (obligatoire ?) pour savoir s'il y faut afficher les chamsp adresse / tel / email


## Deuxième onglet dans le tableau de priorisation

Évoqué lors de la réunion référente précedente, avoir un deuxième onglet pour prioriser les **discussions**. Cela permettra de filtrer quelle sont les points importants, les ateliers à organiser.

## Annoncer les congés sur le forum

Clarrisse va sans doute lancer le sujet. Nous ajouterons ensuite les congés de l'équipe.
