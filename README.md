# Veolia — Capstone
EDHEC Capstone — Veolia GreenUp 2027 — Bioénergie et capacité financière.

Data room privée et auditable : conserver les preuves, tracer les chiffres et préparer les analyses. Les agents proposent ; les humains approuvent et fusionnent les PR.

## Démarrage
1. Lire [AGENTS.md](AGENTS.md) et le [briefing](00_brief/README.md).
2. Consulter [SOURCES.csv](SOURCES.csv) avant toute recherche pour éviter les doublons.
3. Créer une branche `agent/<role>/<objet>` depuis `main`.
4. Déposer les originaux, indexer les sources et documenter les analyses.
5. Mettre à jour [CONTRADICTIONS.md](CONTRADICTIONS.md) et [AI_USAGE_LOG.md](AI_USAGE_LOG.md), puis ouvrir une PR pour validation humaine.

## Classement
| Dossier | Contenu |
| --- | --- |
| 00_brief | Briefing original et cadrage validé |
| 01_veolia | Publications du groupe, résultats et stratégie |
| 02_debt_rating | Dette, maturités, définitions du levier et agences de notation |
| 03_bioenergy | Bioénergie, technologies, marchés et réglementation |
| 04_comparables | Émetteurs comparables et méthodes de comparaison |
| 05_transactions | Acquisitions, cessions, multiples et synergies |
| 06_esg | Indicateurs ESG, méthodologies et limites |
| 07_models | Modèles, hypothèses, formules et sensibilités |
| 99_archive | Versions remplacées, jamais effacées silencieusement |

## Index des sources
CSV UTF-8 avec en-tête, virgule comme séparateur et guillemets CSV pour les champs contenant virgules ou retours à la ligne. Une ligne par version de document ; aucun identifiant réutilisé.
- `source_id` : identifiant stable `SRC-<role>-YYYYMMDD-<slug>`.
- `title, issuer, source_type, topic` : titre, émetteur, nature (primary/secondary/briefing), thème.
- `publication_date` : date publiée ISO YYYY-MM-DD ou `unknown` ; ne pas la déduire de la date de téléchargement ou des métadonnées.
- `retrieved_date, original_url, file_path` : date de collecte, provenance (URL ou référence à une pièce jointe), chemin relatif.
- `sha256` : empreinte des octets originaux ; `page_count, relevant_pages` : pages physiques PDF, numérotées à partir de 1.
- `status` : collected / verified / blocked / superseded. verified signifie contrôle documentaire, pas approbation humaine de l'analyse.
- `collected_by, verified_by, verified_date, notes` : piste d'audit ; champs de vérification vides tant que non contrôlés.

Nom des documents : `<source_id>__<titre-court>.pdf`. Conserver le nom original dans notes. Les nouvelles versions reçoivent un nouvel identifiant et un lien vers l'ancienne.

## Gouvernance
Les profils Source, Verification et Contradiction sont définis dans AGENTS.md, avec prompts de lancement. Aucun agent permanent, calendrier ou accès autonome n'est activé par ces fichiers.
La règle de revue humaine est documentaire. La protection technique de `main` doit être configurée par un administrateur : PR obligatoire, approbation humaine, pas de push direct ni de contournement, selon les options disponibles. Aucune protection n'est réputée active sans vérification.
