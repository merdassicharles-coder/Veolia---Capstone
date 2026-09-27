# Data room — index (catalogue de lecture rapide)

Ce fichier est le point d'entrée pour un agent qui doit répondre à une question sans rouvrir tous les PDF. Il complète [SOURCES.csv](SOURCES.csv), qui reste le registre d'audit faisant foi (provenance, empreinte, statut de vérification).

Convention : `doc_id` ici = `source_id` dans SOURCES.csv pour les sources individuelles, ou un identifiant de résumé groupé (`<theme>_2026-09`) quand plusieurs source_id partagent un même résumé pour des raisons d'efficacité (voir `source_ids` dans le frontmatter de chaque résumé groupé). Un document a un PDF dans `raw/<source_id>.pdf` quand il a pu être téléchargé, un résumé dans `summaries/` et, le cas échéant, des tableaux dans `data/`. Le PDF original du briefing pédagogique reste dans `00_brief/` (ne pas dupliquer dans `raw/`).

Avant toute recherche : consulter ce tableau et [SOURCES.csv](SOURCES.csv) pour éviter les doublons.

| doc_id / groupe | Titre | Émetteur(s) | Thème | Statut | Résumé |
|---|---|---|---|---|---|
| SRC-setup-20260927-capstone-brief | Capstone - Project Briefing | EDHEC | 00_brief | collected | [00_brief/README.md](00_brief/README.md) |
| veolia_greenup_2026-09 | Résultats FY2025, H1 2026, programme GreenUp (4 sources) | Veolia Environnement | 01_veolia | collected | [summaries/veolia_greenup_2026-09.md](summaries/veolia_greenup_2026-09.md) |
| transactions_2026-09 | Water Technologies/CDPQ, Clean Earth/Enviri, tuck-ins, WM/Stericycle (5 sources) | Veolia, Enviri, WM | 05_transactions | collected | [summaries/transactions_2026-09.md](summaries/transactions_2026-09.md) |
| comparables_2026-09 | Comparables cotés eau/déchets dangereux/bioénergie (9 sources) | Xylem, Clean Harbors, Séché, Renewi, EnviTec Biogas, etc. | 04_comparables | collected | [summaries/comparables_2026-09.md](summaries/comparables_2026-09.md) |
| regulation_2026-09 | RED III, IED, CSRD, biométhane France (5 sources) | UE, France | 03_bioenergy / 06_esg | collected | [summaries/regulation_2026-09.md](summaries/regulation_2026-09.md) |
| credit_capacity_2026-09 | Notation crédit, dette nette, capacité financière (5 sources) | Veolia, Moody's, S&P, Fitch | 02_debt_rating | collected | [summaries/credit_capacity_2026-09.md](summaries/credit_capacity_2026-09.md) |

## Journal
- 2026-09-27 — Création de INDEX.md, GAPS.md, workstreams/, raw/, summaries/, data/.
- 2026-09-27 — Collecte par 5 agents de recherche (Veolia, comparables, transactions, régulation, crédit) : 28 nouvelles lignes SOURCES.csv, 5 résumés groupés dans summaries/. Aucun PDF téléchargé physiquement dans raw/ (réseau restreint dans cet environnement, y compris depuis la machine de Lorenzo) — plusieurs sources identifiées sont pourtant des PDF officiels réels hébergés sur veolia.com/renewi.com, listés dans GAPS.md pour téléchargement manuel.

## À faire à chaque ingestion
1. Copier le PDF original dans `raw/<source_id>.pdf` (jamais modifié après coup) — ou, si seule une page web est accessible, le documenter comme preuve provisoire (URL + date de consultation) conformément à AGENTS.md.
2. Écrire un résumé dans `summaries/` (gabarit dans `AGENTS.md` et dans la skill `dataroom-ingest`).
3. Extraire les tableaux utiles dans `data/<source_id>__<table>.csv`, colonne `source_page` obligatoire (uniquement possible avec un PDF ouvert directement).
4. Ajouter la ligne dans `SOURCES.csv` (registre d'audit) et dans le tableau ci-dessus (catalogue de lecture).
5. Signaler toute incertitude dans `GAPS.md`.
