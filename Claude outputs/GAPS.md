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

## Lacunes comblées le 2026-09-27 (téléchargement manuel par Lorenzo)

- GAP-20260927-pdf-download-manuel — Rôle 1 — **partiellement filled.** Lorenzo a téléchargé et déposé 7 PDF officiels dans `raw/`. Contrôlés (SHA-256 + pagination) et passés `status=verified` dans SOURCES.csv, avec résumé individuel page-cité créé pour chacun :
  - Finance_PR_Veolia_2025_results.pdf → SRC-veolia-20260927-fy2025-results ✅
  - Finance_PR_acquisition_water_technologies_solutions_05-07-2025_0.pdf (nommé cp-wts-070525.pdf) → SRC-transactions-20260927-wts-cdpq ✅
  - Veolia_Clean_Earth_Investor_Presentation.pdf → SRC-transactions-20260927-clean-earth-investor-presentation ✅
  - Credit_Opinion_Veolia-Environnement-2Dec2025.pdf → SRC-credit-20260927-moodys-credit-opinion ✅
  - **Bonus (non prévus initialement, ajoutent de la valeur)** : présentation H1 2026 (SRC-veolia-20260927-h1-2026-presentation-bonus), Credit Opinion Moody's 4 mai 2026 (voir avertissement ci-dessous), S&P RatingsDirect Tear Sheet 27 avr. 2026 (SRC-credit-20260927-sp-ratingsdirect-tearsheet-bonus) — comble partiellement GAP-20260927-sp-thresholds.

  **Reste à télécharger** (toujours open, priorité avant le 7 octobre) :
  - Veolia_Finance_PR_H1_2026_results.pdf (communiqué de presse officiel H1 2026 — distinct de la présentation investisseurs déjà obtenue) — URL dans SOURCES.csv, source_id SRC-veolia-20260927-h1-2026-results.
  - Renewi Annual Report and Accounts 2025 (renewi.com) — URL dans SOURCES.csv, source_id SRC-comparables-20260927-renewi-fy2025.

- **GAP-20260927-document-confidentiel-moodys-mai2026** — Rôle 3 — **NOUVELLE LACUNE, PRIORITÉ HAUTE.** Le PDF `SRC-credit-20260927-moodys-credit-opinion-may2026-bonus` (Credit Opinion Moody's daté du 4 mai 2026) porte la mention **"DRAFT - CONFIDENTIAL"** en filigrane sur chaque page, contrairement à la version du 2 décembre 2025 qui n'a aucune mention de ce type. Ce n'est donc apparemment pas une publication publique finalisée. Action requise : demander à Lorenzo la provenance exacte de ce fichier (site officiel ? relais tiers ? autre ?) ; si la légitimité/le caractère public ne peut pas être établi, retirer ce document du data room et ne pas citer ses chiffres (parts d'EBITDA Eau/Déchets 2025 à 48%/32%) dans le rapport final — utiliser à la place SRC-veolia-20260927-fy2025-results et SRC-veolia-20260927-h1-2026-presentation-bonus pour les mêmes informations obtenues par une voie non ambiguë. Statut : open, décision humaine requise (aucune résolution silencieuse, conformément à AGENTS.md).
- GAP-20260927-veolia-debt-maturity-echeancier — Rôle 3 — Profil de maturité de la dette (échéancier par année) toujours introuvable publiquement. Statut : open.
- GAP-20260927-sp-thresholds — Rôle 3 — **partiellement filled** — Le Tear Sheet S&P officiel (SRC-credit-20260927-sp-ratingsdirect-tearsheet-bonus, gratuit) donne une fourchette cible FFO ajusté/dette de 20%-22% sur 2026-2028 pour le maintien du 'BBB' (p.1). Le rapport RatingsDirect complet avec la méthodologie détaillée des seuils reste sous abonnement — statut : open pour cette partie seulement, pourrait nécessiter l'accès bibliothèque EDHEC.
- GAP-20260927-water-comparables-multiples — Rôle 4 — Aucune transaction comparable récente (2024-2026) en eau industrielle avec multiple EV/EBITDA publié trouvée via sources gratuites. Statut : open — pourrait nécessiter Mergermarket/CapitalIQ (accès EDHEC).
- GAP-20260927-greenup-launch-date — Rôle 1 — Date de publication exacte du communiqué de lancement GreenUp : deux dates circulent (fin février vs 6 mars 2024) — non tranchée. Statut : open.
- GAP-20260927-cdpq-press-release — Rôle 1 — Aucun communiqué CDPQ distinct trouvé pour la cession de ses 30% de Water Technologies (seule la source Veolia documente officiellement la transaction côté officiel). Statut : open, faible priorité.

## Lacunes comblées le 2026-09-27 (5 agents de recherche dédiés bioénergie — nouveau dossier 03_bioenergy/)

- GAP-20260927-bioenergy-comparables-depth — Rôle 2 — **filled.** 4 comparables cotés documentés avec données financières complètes (EnviTec Biogas, Verbio, Montauk Renewables, Clean Energy Fuels), fourchette EV/EBITDA ≈5,5x-7,7x hors cas distordus. Positionnement qualitatif d'Engie (BiOZ), TotalEnergies (ex-Fonroche) et EDF documenté (voir 03_bioenergy/documents/02_comparables_cotes.md et 03_majors_energetiques.md). Le constat de rareté structurelle des comparables à l'échelle de Veolia est confirmé plutôt qu'infirmé — c'est en soi un résultat utile pour le mémoire.
- GAP-20260927-greenup-capital-markets-day — Rôle 1 / Rôle 2 — **partiellement filled.** Le PDF du Capital Markets Day GreenUp (29 février 2024) a été localisé en accès libre : https://www.veolia.com/sites/g/files/dvc4206/files/document/2024/03/EN_Master_GreenUp_Strategy%20day.pdf. Les chiffres **8 GW bioénergie / 3 GW flexible à horizon 2030 sont désormais CONFIRMÉS par triple recoupement** de sources officielles Veolia (voir SRC-bioenergy-20260927-4bn-investment-announcement, SRC-bioenergy-20260927-green-financing-framework-2025, SRC-bioenergy-20260927-greenup-cmd-feb2024). En revanche les chiffres de CA sectoriel (12 Md€ / >10 Md€ / 12,3 Md€ selon la source) et de CA/EBITDA du sous-segment bioénergie seul (~615 M€, objectif 4,9 Md€ 2030) restent à vérifier par lecture manuelle directe du PDF — voir CON-20260927-ca-energie-2023-base et 03_bioenergy/documents/01_veolia_booster_bioenergie.md. Statut : partiellement filled, priorité haute pour relecture manuelle avant citation finale.
- GAP-20260927-red-iii-articles — Rôle 5 — **partiellement filled.** EUR-Lex reste inaccessible en lecture directe (rendu JS/robots) depuis cet environnement — seules les métadonnées de la directive (UE) 2023/2413 ont pu être confirmées. Les seuils de réduction GES par filière biomasse ont été trouvés via une source secondaire (CrossCheck Compliance Hub, résumé juridique tiers) : 65%/70%/80% selon la date de mise en service — **à vérifier sur le texte officiel avant citation de premier rang dans le mémoire**. Statut : open pour la vérification finale sur texte officiel.
- GAP-20260927-csrd-stopclock-url — Rôle 5 — **filled.** Référence exacte trouvée : Directive (UE) 2025/794 du 14 avril 2025 (Omnibus I), modifiant les directives 2006/43/CE, 2013/34/UE, (UE) 2022/2464 et (UE) 2024/1760. Voir SRC-bioenergy-20260927-omnibus-i-directive-2025-794.

## Nouvelles lacunes ouvertes le 2026-09-27 (issues des 5 agents bioénergie)

- **GAP-20260927-ca-energie-2023-base** — Rôle 1/2 — Trois formulations différentes du CA "énergie" 2023 servant de base au calcul de la trajectoire GreenUp bioénergie : 12 Md€ (page corporate), >10 Md€ (communiqué Businesswire officiel), 12,3 Md€ (PDF Capital Markets Day, périmètre incluant eau+déchets liés à l'énergie). Voir CONTRADICTIONS.md, CON-20260927-ca-energie-2023-base. Statut : open, décision humaine requise sur quel chiffre retenir dans le mémoire.
- **GAP-20260927-valenton-capacite** — Rôle 1 — Écart entre deux sources sur la capacité de l'unité de biométhane de Valenton : 45 GWh/an (article Environnement Magazine, oct. 2024) vs 163 GWh (PDF Capital Markets Day, fév. 2024). Voir CONTRADICTIONS.md, CON-20260927-valenton-capacite. Statut : open — le communiqué SIAAP original est inaccessible (erreur 403), une troisième source serait nécessaire pour trancher.
- **GAP-20260927-france-textes-403** — Rôle 5 — Deux textes réglementaires français importants sur le biométhane n'ont pu être lus en détail (page Légifrance en erreur 403 au moment de la recherche, référence bibliographique confirmée par recoupement uniquement) : l'arrêté du 10 août 2026 (modificatif le plus récent du régime tarifaire biométhane) et le décret n° 2021-1273 du 30 septembre 2021 (base légale des appels d'offres CRE). Statut : open — à retenter en fetch direct ou à demander à Lorenzo de télécharger via Légifrance.
- **GAP-20260927-nature-energy-multiple-non-officiel** — Rôle 2/4 — Le seul multiple EV/EBITDA trouvé pour une transaction bioénergie majeure (Shell/Nature Energy, ≈24,1x) provient d'une source secondaire d'agrégation M&A (mainsights.io), non confirmée par les parties. Ne pas le citer comme un fait établi dans le mémoire sans le qualifier explicitement d'estimation tierce. Statut : wont_fill (source primaire indisponible gratuitement), à utiliser avec la réserve indiquée.
- **GAP-20260927-loi-climat-resilience-art95-url** — Rôle 5 — URL Légifrance exacte de l'article 95 de la loi n° 2021-1104 du 22 août 2021 (certificats de production de biométhane sans soutien public) non capturée précisément. Statut : open, faible priorité.
