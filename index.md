---
layout: default
title: Softto — Documentation
---

Plateforme web de gestion de tontines pour les groupes et associations communautaires camerounaises : épargne, prêts à dette révolvante (intérêts composés mensuels), remboursements, répartition des intérêts, tontine rotative (« ordre de bouffe »), collectes spéciales, pointage des séances et rapports imprimables — le tout en multi-groupes, avec abonnement par groupe.

Ce site contient uniquement la documentation publique de Softto. Le code source est privé.

📖 [Guide utilisateur complet](GUIDE_UTILISATEUR.html)

## Aperçu

Softto fonctionne en mode SaaS multi-groupes : chaque association (« groupe ») dispose de son propre espace isolé, avec ses membres, ses cycles de tontine, son épargne et ses comptes séparés des autres groupes.

### Fonctionnalités principales

- Tableau de bord financier (épargne, prêts, intérêts, dettes, liquidités)
- Épargne mensuelle et prêts à intérêts composés
- Tontine rotative avec ordre de bouffe (tirage au sort ou ordre du comité)
- Cotisations de caisse, collectes spéciales, répartition des intérêts
- Réunions et pointage des présences
- Import CSV et export PDF/Excel des rapports, aux couleurs de l'association
- Rôles et permissions par groupe (administrateur, trésorier, membre)
- Bilingue français / anglais

### Pile technique

| Composant | Technologie |
|---|---|
| Framework | Laravel 12 (PHP 8.2+) |
| Base de données | MySQL / MariaDB |
| Front-end | Blade, Tailwind CSS, Alpine.js, Vite |
| Rôles & permissions | spatie/laravel-permission (multi-groupes) |
| Journal d'activité | spatie/laravel-activitylog |
| Exports | maatwebsite/excel, barryvdh/laravel-dompdf |

## Licence et accès

Softto est un projet propriétaire. Le code source n'est pas public. Pour toute question sur la plateforme ou son utilisation, référez-vous au [guide utilisateur](GUIDE_UTILISATEUR.html).
