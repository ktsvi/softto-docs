---
layout: default
title: Guide utilisateur — Softto
---

# Guide utilisateur — Softto

Plateforme de gestion de tontine · Épargne · Prêts · Intérêts · Réunions · Abonnements

[← Retour à l'accueil](index.html)

## 1. Présentation

Softto est une plateforme web de gestion de tontine conçue pour les réunions, associations et groupes communautaires — avec une adaptation aux réalités camerounaises (monnaie XAF, Mobile Money, langue française). Elle digitalise les pratiques traditionnelles de tontine : épargne, prêts, remboursements, répartition des intérêts, réunions et pointage.

L'application fonctionne en mode SaaS multi-groupes : chaque groupe (« organisation ») dispose de son propre espace isolé. Le modèle économique repose sur un abonnement mensuel ou annuel payé par chaque groupe.

### Fonctionnalités principales

- **Tableau de bord financier** : épargne mobilisée, montant prêté, intérêts générés, remboursements, dettes restantes et liquidités disponibles.
- **Gestion de l'épargne** : saisie et suivi mensuel des contributions par membre.
- **Gestion des prêts** : montant, durée, taux mensuel, intérêts dus, échéance et statut (en cours, soldé, en retard).
- **Remboursements** : suivi par membre avec distinction capital / intérêts et historique détaillé.
- **Répartition des intérêts** : calcul au prorata des parts-mois et génération de rapports de distribution.
- **Suivi des dettes** : capital restant dû par membre, intérêts restants et alertes de retard.
- **Tontine rotative** : ordre de bouffe, parts multiples, cagnottes réparties automatiquement.
- **Collectes spéciales** : naissance, deuil, mariage — montant fixe par membre, échéance au choix.
- **Réunions & pointage** : gestion des présences, rapport de séance.
- **Imports / Exports** : import CSV des membres et de l'épargne ; export PDF et Excel des rapports, aux couleurs de votre association.
- **Abonnements & paiements** : plans tarifaires, paiement Mobile Money (MTN MoMo, Orange Money) ou validation manuelle.
- **Sécurité** : authentification, rôles et permissions par groupe, journal d'activité, comptes réutilisables entre plusieurs groupes.
- **Bilingue** : français (par défaut) et anglais.

### Les trois niveaux d'utilisation

| Niveau | Rôle | Ce qu'il fait |
|---|---|---|
| Plateforme | Super-administrateur | Propriétaire de Softto : crée les groupes, gère les plans d'abonnement et valide les paiements. |
| Groupe | Admin de groupe | Responsable d'une tontine : membres, épargne, prêts, intérêts, réunions, imports/exports, abonnement. |
| Groupe | Trésorier | Saisit l'épargne, les remboursements, le pointage, crée des prêts et exporte les rapports. |
| Groupe | Membre | Consulte le tableau de bord et ses propres données. |

## 2. Comptes, rôles et permissions

Softto distingue le super-administrateur de la plateforme des rôles internes à chaque groupe. Les permissions sont propres à chaque groupe : un même utilisateur peut être administrateur d'un groupe et simple membre d'un autre, avec un seul compte de connexion.

### Matrice des permissions par rôle

| Permission | Admin groupe | Trésorier | Membre |
|---|:---:|:---:|:---:|
| Voir le tableau de bord | ✓ | ✓ | ✓ |
| Gérer les membres | ✓ | — | — |
| Créer des prêts | ✓ | ✓ | — |
| Gérer les prêts (modifier/supprimer) | ✓ | — | — |
| Saisir l'épargne | ✓ | ✓ | — |
| Saisir les remboursements | ✓ | ✓ | — |
| Gérer le pointage | ✓ | ✓ | — |
| Répartir les intérêts | ✓ | — | — |
| Exporter les rapports | ✓ | ✓ | — |
| Importer des CSV | ✓ | — | — |
| Gérer l'abonnement | ✓ | — | — |
| Paramètres du groupe | ✓ | — | — |
| Voir ses propres données | ✓ | ✓ | ✓ |

## 3. Utilisation — Super-administrateur (plateforme)

Le super-administrateur gère l'ensemble de la plateforme. C'est lui qui crée les groupes clients, définit les offres et valide les abonnements.

- **Tableau de bord plateforme** : vue d'ensemble — nombre de groupes, abonnements actifs, paiements en attente de validation.
- **Créer et gérer les groupes** : nom, monnaie, langue et statut. Le groupe dispose aussitôt de son espace et de ses rôles.
- **Gérer les plans d'abonnement** : créer, modifier ou désactiver un plan à tout moment.
- **Valider les paiements d'abonnement** : chaque groupe déclare son paiement (Mobile Money ou autre) ; le super-administrateur vérifie la référence de transaction puis valide ou rejette.

> Si un groupe n'a pas d'abonnement actif, ses membres sont automatiquement redirigés vers la page d'abonnement et ne peuvent plus saisir de données — seuls le tableau de bord et la page de paiement restent accessibles, le temps de régulariser.

## 4. Utilisation — Administrateur de groupe (tontine)

L'administrateur d'un groupe travaille dans l'espace de son organisation. Voici le cycle de vie complet d'une tontine.

- **Tableau de bord du groupe** : synthèse financière en temps réel — épargne mobilisée, montant prêté, intérêts générés, remboursements encaissés, dettes restantes, liquidités disponibles.
- **Gérer les membres** : ajouter, modifier ou archiver un membre ; le relier à un compte utilisateur pour lui donner accès à ses propres données. Pour un groupe existant, l'import CSV est plus rapide qu'une saisie manuelle.
- **Saisir l'épargne mensuelle** : par période, par membre ; les totaux se recalculent automatiquement.
- **Enregistrer un prêt** : bénéficiaire, capital, durée, taux mensuel, date de décaissement. Softto calcule automatiquement la référence, les intérêts dus, le total à rembourser et la date d'échéance.
  - *Intérêts dus = Capital × Durée (mois) × Taux mensuel*
  - *Total dû = Capital + Intérêts.* Le statut passe de « en cours » à « soldé » une fois remboursé, ou « en retard » si l'échéance est dépassée.
- **Saisir les remboursements** : montant reçu et répartition capital / intérêts ; le statut du prêt se met à jour automatiquement.
- **Répartir les intérêts** : calcul au prorata des « parts-mois » de chaque membre (épargne × durée). Chaque campagne de répartition peut être consultée et exportée.
- **Suivre les dettes** : vue par membre du capital restant dû, des intérêts restants et du total à payer, avec mise en évidence des retards.
- **Réunions et pointage** : créer une réunion, cocher les présences ; les présences sont archivées pour la traçabilité.
- **Importer des données (CSV)** : membres, ou épargne. Les lignes valides sont créées, un rapport signale les éventuelles erreurs.
- **Exporter les rapports** : épargne, prêts, dettes, répartition des intérêts — en Excel et/ou PDF, avec le logo et le nom de l'association.
- **Gérer l'abonnement du groupe** : choisir un plan, déclarer le paiement, en attente de validation par le super-administrateur.

## 5. Utilisation — Trésorier et Membre

### Le trésorier

Le trésorier assure la saisie financière courante, sans les droits d'administration. Il peut saisir l'épargne mensuelle, enregistrer les remboursements, créer des prêts (mais pas les modifier/supprimer), gérer le pointage des réunions, exporter les rapports et consulter le tableau de bord. Il n'a pas accès à la gestion des membres, à la répartition des intérêts, aux imports ni à l'abonnement.

### Le membre

Un membre dispose d'un accès en lecture seule. Il consulte le tableau de bord du groupe et ses propres données (épargne, prêts, dettes le concernant), sans possibilité de modification. Selon le réglage choisi par l'association, il peut aussi voir les comptes de tous les membres (transparence totale), coordonnées masquées.

---

*Ce guide décrit l'usage de Softto. La documentation technique de déploiement n'est pas publique.*
