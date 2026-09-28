# Veolia — Capstone : data room

Base documentaire commune pour GreenUp, bioénergie, dette et notation, avec comparables, transactions et réglementation. Les sources historiques antérieures au périmètre 2024–2026 restent conservées.

Commencer par [INDEX.md](INDEX.md), puis [le catalogue des sources](SOURCE_CATALOG.md). Le registre unique est [SOURCES.csv](SOURCES.csv). Les contrôles et limites figurent dans [CONSOLIDATION_REPORT.md](CONSOLIDATION_REPORT.md).

## Où trouver quoi
| Emplacement | Fonction |
| --- | --- |
| [00_brief](00_brief/README.md) | Briefing original et périmètre pédagogique |
| [01_veolia](01_veolia/README.md) | Groupe, GreenUp et résultats |
| [02_debt_rating](02_debt_rating/README.md) | Dette, notations et capacité financière |
| [03_bioenergy](03_bioenergy/README.md) | Cinq analyses bioénergie et vue des sources associées |
| [04_comparables](04_comparables/README.md) | Comparables et méthodes de valorisation |
| [05_transactions](05_transactions/README.md) | Acquisitions et multiples publiés |
| [06_esg](06_esg/README.md) | Réglementation et durabilité |
| [07_models](07_models/README.md) | Futurs modèles, hypothèses et calculs |
| [raw](raw/README.md) | PDF originaux, jamais réécrits |
| [summaries](summaries/README.md) | Résumés et points de contrôle des PDF |
| [data](data/README.md) | Historique des corrections et doublons signalés |
| [workstreams](workstreams/README.md) | Répartition du travail entre les rôles du projet |
| [99_archive](99_archive/README.md) | Versions antérieures conservées pour audit |
| [Claude outputs](<Claude outputs/README.md>) | Lot importé original, conservé intégralement |

## Comment lire les statuts
98 références sont enregistrées, dont 66 issues du lot bioénergie. Ce ne sont pas 98 documents téléchargés : huit PDF sont présents, briefing compris. Deux groupes d’URL identiques sont signalés, sans supprimer d’identifiant.

- `verified` : six documents ont fait l’objet d’un contrôle documentaire ciblé ; cela ne valide pas automatiquement chaque chiffre de toutes les analyses.
- `collected` : 53 références identifiées restent à contrôler.
- `blocked` : 39 références comportent un obstacle explicite, notamment une date inconnue. Elles restent consultables, mais ne fondent pas les conclusions validées.

Les arbitrages restent dans [CONTRADICTIONS.md](CONTRADICTIONS.md) et les travaux à terminer dans [GAPS.md](GAPS.md). Les fichiers historiques ne constituent pas des instructions actuelles.

## Fonctionnement des agents
Les trois rôles sont définis dans [AGENTS.md](AGENTS.md) : collecte → vérification → comparaison. Ils ne sont pas des services qui tournent seuls ; aucune automatisation de recherche n’est configurée ici. Les agents peuvent ajouter et corriger des contenus sur `agent/*` sans validation préalable de chaque ajout, en conservant les versions et en ouvrant une PR. La fusion dans `main` reste humaine. Les interventions sont consignées dans [AI_USAGE_LOG.md](AI_USAGE_LOG.md).

La visibilité observée du dépôt est publique au moment de la consolidation ; cette opération ne modifie pas ses paramètres.
