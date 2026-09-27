# Lacunes et zones d'incertitude

Registre des trous connus dans la data room : ce qui manque, ce qui est incertain, ce qui reste à vérifier. Un registre vide ou court ne prouve rien — le tenir à jour à chaque ingestion et avant chaque checkpoint.

Statuts : `open` (personne n'a encore comblé la lacune), `in_progress`, `filled` (source ajoutée, à vérifier), `wont_fill` (justifié).

## Modèle à copier
- gap_id : GAP-YYYYMMDD-<slug>
- Rôle / workstream concerné :
- Ce qui manque et pourquoi c'est nécessaire :
- Piste(s) de source pour combler :
- Statut :
- Ouvert par / date :
- Comblé par / date / source_id :

## Lacunes comblées le 2026-09-27 (collecte des 5 agents — à vérifier par un humain ou un Verification Agent)

- GAP-20260927-veolia-2025-annual-report — **filled** — Résultats FY2025 et H1 2026 trouvés (communiqués PDF officiels sur veolia.com), voir SRC-veolia-20260927-fy2025-results et SRC-veolia-20260927-h1-2026-results. Le Document d'enregistrement universel (URD) lui-même n'a en revanche pas été localisé — reste à chercher (piste : veolia.com/en/investors ou AMF/info-financiere.fr).
- GAP-20260927-veolia-debt-maturity — **partiellement filled** — Les deux chiffres de dette nette (20 764 M€ au 30/06/2025, 24 548 M€ au 30/06/2026) et la définition du levier sont confirmés à la publication officielle (SRC-veolia-20260927-h1-2026-results). Le **profil de maturité de la dette (échéancier par année) reste introuvable publiquement** — statut : open pour cette partie.
- GAP-20260927-rating-reports — **partiellement filled** — Notations Moody's (Baa1 stable, Credit Opinion PDF officiel republié par Veolia, seuils de dégradation FFO/dette nette trouvés) et S&P (BBB stable, relais Cbonds) documentées. **Découverte importante : Fitch ne note plus Veolia depuis le 12/06/2024** (notation retirée) — voir CONTRADICTIONS.md, CON-20260927-fitch-rating. Rapports complets (RatingsDirect S&P) toujours inaccessibles (abonnement) — statut : open pour cette partie.
- GAP-20260927-water-technologies-clean-earth — **filled** — Communiqué officiel Veolia (PDF, SRC-transactions-20260927-wts-cdpq) et communiqué Enviri Corporation (GlobeNewswire, SRC-transactions-20260927-clean-earth-enviri) trouvés et confirment les chiffres du briefing pédagogique.
- GAP-20260927-comparables — **filled** — Comparables identifiés pour les 3 boosters (voir summaries/comparables_2026-09.md). Le booster bioénergie reste pauvre en comparables (un seul pure-player coté, EnviTec Biogas) — voir nouvelle lacune GAP-20260927-bioenergy-comparables-depth ci-dessous.
- GAP-20260927-bioenergy-regulation — **filled** — RED III, IED, CSRD et réglementation française biométhane documentées (voir summaries/regulation_2026-09.md). Quelques articles opérationnels fins non extraits (voir nouvelles lacunes ci-dessous).
- GAP-20260927-tuck-ins-2025 — **wont_fill, confirmé** — Le communiqué officiel Veolia North America confirme explicitement l'absence de prix individuel public ; seul un montant agrégé non ventilable (~350 M$ sur 5 transactions dont 2 hors périmètre) est disponible. Ne pas utiliser ce chiffre comme proxy de valorisation individuelle.

## Lacunes ouvertes au 2026-09-27 (nouvelles ou toujours ouvertes après collecte)

- GAP-20260927-pdf-download-manuel — Rôle 1 — **Priorité avant le checkpoint du 7 octobre.** Plusieurs sources collectées sont des PDF officiels réels mais n'ont pas pu être téléchargés physiquement dans `raw/` depuis cet environnement (réseau restreint, y compris depuis la machine de Lorenzo). À télécharger manuellement (navigateur normal) et déposer dans `raw/<source_id>.pdf` : Finance_PR_Veolia_2025_results.pdf, Veolia_Finance_PR_H1_2026_results.pdf, Finance_PR_acquisition_water_technologies_solutions_05-07-2025_0.pdf, Veolia_Clean_Earth_Investor_Presentation.pdf, Credit_Opinion_Veolia-Environnement-2Dec2025.pdf, Renewi Annual Report and Accounts 2025 (renewi.com). URLs exactes dans SOURCES.csv. Une fois téléchargés : calculer le SHA-256, mettre à jour SOURCES.csv (sha256, page_count, status=verified après contrôle) et créer un résumé individuel par doc_id plutôt que le résumé groupé provisoire actuel. Statut : open.
- GAP-20260927-veolia-debt-maturity-echeancier — Rôle 3 — Profil de maturité de la dette (échéancier par année) toujours introuvable publiquement. Statut : open.
- GAP-20260927-sp-thresholds — Rôle 3 — Détail méthodologique des seuils de dégradation S&P (rapport RatingsDirect complet, sous abonnement). Statut : open — pourrait nécessiter l'accès bibliothèque EDHEC.
- GAP-20260927-bioenergy-comparables-depth — Rôle 2 — Le booster bioénergie manque de comparables cotés à l'échelle de Veolia (seul EnviTec Biogas identifié, échelle ~100x plus petite). Verbio (Allemagne) n'a pas été recherché spécifiquement — piste à explorer. Données financières 2024-2025 de la division biométhane Engie non accessibles (PDF sur engie.com non ouverts dans cet environnement) ; CA/EBITDA de l'activité biogaz TotalEnergies non publiés. Statut : open.
- GAP-20260927-water-comparables-multiples — Rôle 4 — Aucune transaction comparable récente (2024-2026) en eau industrielle avec multiple EV/EBITDA publié trouvée via sources gratuites. Statut : open — pourrait nécessiter Mergermarket/CapitalIQ (accès EDHEC).
- GAP-20260927-greenup-capital-markets-day — Rôle 1 / Rôle 2 — Le Capital Markets Day GreenUp (février 2024), qui documenterait vraisemblablement le booster "bioénergie et efficacité énergétique" en détail, n'a pas été localisé en accès libre. Chiffres provisoires (8 GW bioénergie 2030, 3 GW flexible, 12 Md€ CA sectoriel 2023) trouvés via un résumé automatisé non confirmé indépendamment — **ne pas les utiliser sans confirmation**. Statut : open — priorité haute pour le workstream 2.
- GAP-20260927-red-iii-articles — Rôle 5 — Articles opérationnels détaillés de RED III sur les critères de durabilité biomasse par filière non extraits (rendu JavaScript côté EUR-Lex). Statut : open.
- GAP-20260927-csrd-stopclock-url — Rôle 5 — URL EUR-Lex exacte de la directive "stop-the-clock" (Omnibus I, report CSRD) non retrouvée précisément. Statut : open.
- GAP-20260927-greenup-launch-date — Rôle 1 — Date de publication exacte du communiqué de lancement GreenUp : deux dates circulent (fin février vs 6 mars 2024) — non tranchée. Statut : open.
- GAP-20260927-cdpq-press-release — Rôle 1 — Aucun communiqué CDPQ distinct trouvé pour la cession de ses 30% de Water Technologies (seule la source Veolia documente officiellement la transaction côté officiel). Statut : open, faible priorité.
