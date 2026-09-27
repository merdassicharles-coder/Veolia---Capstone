# Bilan de consolidation — 27 septembre 2026

## Périmètre et conservation
Base reçue : branche agent/setup-data-room, commit `7f994637f9246e45809688077c68e43308e226fe`. Main était au commit `07b0a5ac81a029f024234b68ee249b532caf2ad1`. La proposition intègre les ajouts présents sur la branche de travail et la consolidation, sans fusion automatique.

Les 61 chemins de fichiers préexistants sont conservés. Tous les PDF, le ZIP et les fichiers préexistants de Claude outputs restent identiques octet par octet. Les Markdown/CSV corrigés disposent d’une copie exacte dans 99_archive/20260927-before-consolidation ; le lot Claude reste à son emplacement d’origine. Le registre bioénergie extrait du ZIP est également archivé. Aucun identifiant source supprimé, aucun déplacement destructif.

## Organisation obtenue
Les deux registres sont réunis dans SOURCES.csv : 98 identifiants, dont les 66 du lot bioénergie. Le catalogue et la vue bioénergie dérivent du registre racine. Les cinq analyses du ZIP sont maintenant dans 03_bioenergy/documents. README et INDEX donnent les points d’entrée ; raw contient les originaux, summaries les résumés, data les traces de contrôle, workstreams la répartition des travaux.

Deux groupes d’URL identiques sont signalés dans data/source_aliases.csv. Ils ne comptent pas comme preuves indépendantes. Les 23 identifiants de lacunes et les quatre contradictions historiques sont conservés ; une cinquième contradiction documente une divergence interne du rapport S&P.

## Niveau de contrôle réel
| État | Nombre | Sens |
| --- | --- | --- |
| verified | 6 | Contrôle documentaire et relecture ciblée ; pas validation exhaustive de chaque affirmation dérivée |
| collected | 53 | Références conservées, contrôle de fond incomplet |
| blocked | 39 | Obstacle explicite, souvent date inconnue ; aucune suppression |
| PDF présents | 8 | Sept documents financiers et briefing ; empreintes et pagination contrôlées |

La vérification est effectuée par Codex au cours de la consolidation, pas par un deuxième intervenant indépendant. Les six statuts verified correspondent à FY2025, H1 présentation, WTS, Clean Earth, Moody’s décembre et S&P avril. Moody’s mai reste blocked malgré l’intégrité confirmée ; le briefing reste blocked faute de date de publication confirmée. Les autres références, notamment réglementaires et comparables, ne sont pas certifiées.

Pages ciblées : FY2025 1, 3–5, 10–11, 15 ; H1 1, 5, 18, 29, 35, 38 ; WTS 1–2 ; Clean Earth 1, 3, 6, 15 ; Moody’s décembre 1–2 ; Moody’s mai 1–2 ; S&P 1–4. Contrôle visuel ciblé des tableaux FY2025 10–11 et H1 18, et des critères S&P 3 ; lecture textuelle des autres pages, intégrité et pagination de tous les PDF. Le briefing a fait l’objet d’une recherche textuelle sur ses pages et d’un contrôle ciblé de la page 18 ; cela ne valide pas tout le briefing.

## Corrections de fond
- FY2025 : date du registre alignée sur la couverture ; données de segment retrouvées et citées pages PDF 10–11 dans le résumé. Ne pas assimiler ce segment élargi à la bioénergie seule.
- H1 : publication précisément datée, base des variations et distinction réalisé/prévision clarifiées. URL officielle retrouvée et empreinte identique au PDF reçu.
- S&P : prévisions distinguées des critères de notation ; pages pertinentes ajoutées, divergence texte/tableau inscrite dans CONTRADICTIONS.md.
- Moody’s : les formulations qualitatives ne sont pas transformées en seuils mathématiques exacts. La [page officielle Veolia](https://www.veolia.com/en/veolia-group/finance/analysts-and-investors/debt-and-ratings) confirme la provenance publique du PDF de mai ; son filigrane laisse sa finalité éditoriale à confirmer. Aucune suppression préconisée.
- Fitch : attribution au briefing non étayée, proposition de requalification visible, sans résolution humaine simulée.
- EDF/Suez : statistiques mondiales et nationales séparées des capacités d’EDF ; actifs du nouveau Suez non attribués automatiquement à Veolia. Contrôles web ciblés, pas validation globale des comparables.
- Multiples : fourchette importée retirée des recommandations validées ; cours, périodes et définitions doivent être homogénéisés.
- Contradictions : plusieurs publications du même émetteur ne sont pas indépendantes ; une borne supérieure/inférieure ne permet pas un écart exact. Aucun arbitrage silencieux.

## Traçabilité et limites
data/consolidation_source_changes.csv conserve les changements champ par champ ; des valeurs peuvent y apparaître à plusieurs étapes. Les notes originales du registre sont explicitement historiques, parfois dépassées : les colonnes courantes, ce rapport et les résumés corrigés font foi. Les dates partielles ne deviennent pas des dates exactes ; un résumé n’est plus présenté comme le fichier source. Les URL inconnues ne sont pas des liens cliquables fictifs.

Résultats structurels : [data/validation_results.json](data/validation_results.json). Contrôles : conservation des fichiers, copies historiques, unicité des identifiants, cohérence du sous-registre, dates, statuts, empreintes, pagination, références source, liens locaux actifs, conservation des identifiants de lacunes/contradictions. Les archives immuables sont exclues du contrôle des liens de navigation, puisque leurs anciens chemins peuvent ne plus correspondre à leur emplacement.

La consolidation ne constitue pas une nouvelle collecte exhaustive de 2024–2026. Priorités restantes : archiver les originaux absents, relire le CMD et l’URD, extraire l’échéancier, compléter les citations, recalculer les comparables et contrôler les textes réglementaires. Les cinq analyses importées restent des documents de travail, avec leurs limites affichées. Pas de modèle financier validé à ce stade.
