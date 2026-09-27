# Data room — index (catalogue de lecture rapide)

Ce fichier est le point d'entrée pour un agent qui doit répondre à une question sans rouvrir tous les PDF. Il complète [SOURCES.csv](SOURCES.csv), qui reste le registre d'audit faisant foi (provenance, empreinte, statut de vérification).

Convention : `doc_id` ici = `source_id` dans SOURCES.csv (mêmes identifiants, pas de double numérotation). Un document a un PDF dans `raw/<source_id>.pdf`, un résumé dans `summaries/<source_id>.md` et, le cas échéant, des tableaux dans `data/<source_id>__<table>.csv`. Le PDF original du briefing pédagogique reste dans `00_brief/` (ne pas dupliquer dans `raw/`).

Avant toute recherche : consulter ce tableau et [SOURCES.csv](SOURCES.csv) pour éviter les doublons.

| doc_id | Titre | Émetteur | Type | Thème | Publié | Statut | Résumé | CSV |
|---|---|---|---|---|---|---|---|---|
| SRC-setup-20260927-capstone-brief | Capstone - Project Briefing | EDHEC | briefing | 00_brief | unknown | collected | [00_brief/README.md](00_brief/README.md) | 0 |

## Journal
- 2026-09-27 — Création de INDEX.md, GAPS.md, workstreams/, raw/, summaries/, data/ ; aucun document collecté au-delà du briefing initial à ce stade.

## À faire à chaque ingestion
1. Copier le PDF original dans `raw/<source_id>.pdf` (jamais modifié après coup).
2. Écrire `summaries/<source_id>.md` (gabarit dans `AGENTS.md` et dans la skill `dataroom-ingest`).
3. Extraire les tableaux utiles dans `data/<source_id>__<table>.csv`, colonne `source_page` obligatoire.
4. Ajouter la ligne dans `SOURCES.csv` (registre d'audit) et dans le tableau ci-dessus (catalogue de lecture).
5. Signaler toute incertitude dans `GAPS.md`.
