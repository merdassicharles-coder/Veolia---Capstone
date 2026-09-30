# Contradictions et divergences à instruire

Registre consolidé au 2026-09-27. Les quatre identifiants historiques sont conservés ; une divergence interne supplémentaire est ajoutée. Aucun arbitrage humain ni résolution n’est simulé. Historique complet : [registre antérieur](99_archive/20260927-before-consolidation/CONTRADICTIONS.md) et [lot bioénergie original](<Claude outputs/CONTRADICTIONS.md>).

## CON-20260927-dechets-dangereux-cible-2027
Statut : **investigating**. Signalement historique : cible du briefing versus communications GreenUp (SRC-setup-20260927-capstone-brief, SRC-veolia-20260927-greenup-launch, SRC-veolia-20260927-greenup-strategic-page).
Les valeurs historiques et leurs références incomplètes restent dans les versions liées ci-dessus. Relever les pages, dates et définitions exactes avant de retenir une base de calcul. Plusieurs publications Veolia ne constituent pas des preuves indépendantes. Aucune cible n’est arbitrée ici. Décision humaine : en attente.

## CON-20260927-fitch-rating
Statut : **proposed_resolution**, proposition de requalification en attribution non étayée, à valider humainement.
La précédente entrée attribuait « S&P/Fitch BBB » au briefing. Le contrôle du texte des 52 pages ne retrouve aucune occurrence de Fitch ; le contrôle ciblé de la page PDF 18 montre les mentions BBB/Baa1. Référence : SRC-setup-20260927-capstone-brief | 00_brief/SRC-setup-20260927-capstone-brief__capstone-project-briefing.pdf | page PDF 18 | publication unknown. Cela ne justifie pas l’attribution antérieure à une troisième agence.
La référence secondaire SRC-credit-20260927-fitch-withdrawal reste conservée, sans confirmation primaire nouvelle du retrait. L’absence de Fitch dans un rapport Moody’s ou S&P ne prouve pas le retrait. Ne pas présenter ce signalement comme une contradiction avérée entre le briefing et Fitch. Historique conservé, aucune suppression. Décision humaine : en attente.

## CON-20260927-ca-energie-2023-base
Statut : **investigating**. Les trois formulations historiques proviennent de SRC-bioenergy-20260927-near-me-greenup-page, SRC-bioenergy-20260927-4bn-investment-announcement et SRC-bioenergy-20260927-greenup-cmd-feb2024.
Une borne « supérieur à » et deux montants de périmètres potentiellement différents ne forment pas nécessairement une contradiction. Retirer l’interprétation antérieure d’un écart arithmétique exact ; ne pas assimiler énergie totale et bioénergie seule. Le sous-chiffre issu d’extraction CMD reste non validé faute de relecture des pages. Les trois publications sont du même émetteur. Aucune base chiffrée n’est arbitrée. Décision humaine : en attente.

## CON-20260927-valenton-capacite
Statut : **investigating**. Signalement reçu entre SRC-bioenergy-20260927-valenton-biomethane-siaap et SRC-bioenergy-20260927-greenup-cmd-feb2024 ; valeurs historiques conservées dans le lot original.
Récupérer les pages originales et distinguer capacité, production, injection, biogaz/biométhane et période. La différence peut provenir de grandeurs non comparables. La préférence antérieure pour l’article le plus récent n’est pas une validation. Aucune valeur n’est retenue pour le modèle sans ce rapprochement. Décision humaine : en attente.

## Journal de correction
Codex, 2026-09-27 : consolidation des deux registres, correction de l’attribution Fitch, retrait des conclusions d’indépendance des publications Veolia et de l’écart arithmétique non démontré ; aucun passage en resolved.

## Gabarit pour une nouvelle divergence
Identifiant stable ; objet ; preuves A/B avec source_id + document + page + date + unité + période + périmètre ; impact ; hypothèses ; contrôles réalisés ; statut ; proposition ; décision humaine nominative et datée ; historique.

## CON-20260927-sp-ffo-forecast
Statut : **open**. Détecté par Codex le 2026-09-27.
- Preuve A : prévision narrative FFO ajusté/dette de 20–22% sur 2026–2028, page PDF 1.
- Preuve B : tableau 19–20% en 2026, 20–21% en 2027, 21–22% en 2028, page PDF 4.
- Source commune : SRC-credit-20260927-sp-ratingsdirect-tearsheet-bonus | raw/SRC-credit-20260927-sp-ratingsdirect-tearsheet-BONUS.pdf | publication 2026-04-27.
- Impact : le point bas annuel retenu dans un scénario de capacité financière varie selon la série.
- Hypothèse : synthèse narrative arrondie ou incohérence rédactionnelle ; non tranchée. Conserver les deux formulations, distinguer prévisions et critères de notation, demander clarification avant arbitrage.
- Décision humaine : en attente. Aucun chiffre corrigé dans le PDF.

## Ajouts du 30 septembre 2026 — contrôle du nouveau lot

## CON-20260928-dette-fy2025-ppa

- Objet : deux présentations de la dette nette de clôture au 31 décembre 2025, groupe Veolia, M€.
- Preuve A : **19 657 M€**, avec ligne de retraitement **−164 M€** au titre de la réévaluation des dettes acquises de Suez. `[SRC-veolia-20260928-revue-financiere-fy2025 | raw/SRC-veolia-20260928-revue-financiere-fy2025.pdf | p. PDF 24, tableau Structure of the net financial debt et note 1 | publication 2026-02-26 | clôture 2025-12-31]`.
- Preuve B : **19 821 M€**, valeur comparative de fin 2025 dans le tableau des chiffres clés. `[SRC-veolia-20260928-amendement-urd-2025-rapport-semestriel-h1-2026 | raw/SRC-veolia-20260928-amendement-urd-2025-rapport-semestriel-h1-2026.pdf | p. PDF 6 (imprimée 4), ligne Net financial debt - Closing | publication 2026-07-30 | clôture 2025-12-31]`.
- Rapprochement explicite : le tableau de A donne **29 518 − 8 021 − 1 952 + 276 − 164 = 19 657 M€** (emprunts, trésorerie, actifs liquides et financiers, dérivés de couverture, retraitement PPA). Sans la dernière ligne, **19 821 M€**. Toutes les entrées, unité M€, périmètre groupe et date de clôture sont celles de A p.24. L'écart de **164 M€ = 19 821 − 19 657** correspond exactement au retraitement de définition, et ne constitue pas une hausse économique démontrée de la dette.
- Appui supplémentaire : les comptes consolidés FY2025 portent **19 821 M€** dans le tableau des échéances note 8.3.2.1, après dettes et dérivés moins trésorerie et actifs financiers, sans la ligne de retraitement PPA. `[SRC-veolia-20260928-comptes-consolides-fy2025 | raw/SRC-veolia-20260928-comptes-consolides-fy2025.pdf | p. PDF 66 | publication 2026-02-26 | clôture 2025-12-31]`. Ce passage a été contrôlé par extraction ; pas de revue visuelle de cette page.
- Nuance : B présente aussi **19 657 M€** dans le corps de la revue financière (p. PDF 25, imprimée 23) et conserve la définition hors réévaluation PPA (section 3.5.2). Le tableau récapitulatif et le corps emploient donc deux bases sous le même intitulé apparent. Ne pas traiter la valeur de B comme un retraitement rétroactif officiellement annoncé.
- Contrôles : pages A24 et B6 rendues puis inspectées visuellement ; note PPA lue ; calcul du pont contrôlé. Aucun PDF modifié.
- Impact : retenir une définition stable pour les variations de dette et le levier ; conserver les deux valeurs et leur pont. Un choix incohérent ferait varier artificiellement la capacité calculée.
- Statut : **proposed_resolution**. Proposition : requalifier l'écart économique en différence de définition, et conserver un signalement de présentation hétérogène dans B. Décision humaine : en attente, validateur/date non renseignés.

## CON-20260928-engie-pepsico-date

- Objet : date du communiqué ENGIE–PepsiCo UK.
- Preuve A : en-tête **January 21, 2025**. `[SRC-comparables-20260928-engie-signs-a-10-year-biomethane-purchase-agreement-with-pepsico-uk | raw/SRC-comparables-20260928-engie-signs-a-10-year-biomethane-purchase-agreement-with-pepsico-uk.pdf | p. PDF 1 | publication unknown : date imprimée 2025-01-21]`.
- Preuve B : page officielle portant **Published on January 21, 2026**, avec pièce jointe datée **20/01/2026** dans le kit média. Document web du même émetteur, sans page PDF : https://en.newsroom.engie.com/news/engie-signs-a-10-year-biomethane-purchase-agreement-with-pepsico-its-first-in-the-united-kingdom-b8ada-314df.html ; consultation 2026-09-28. Référence web de provenance associée au même source_id, pas preuve indépendante.
- Contrôles : page PDF 1 rendue et inspectée visuellement, date 2025 confirmée ; page web lue ; conflit non imputable à une extraction automatique.
- Hypothèses : coquille de millésime dans le PDF, republication ou version documentaire différente. Aucune hypothèse arbitrée.
- Impact : datation fiable de la transaction et comparabilité des objectifs non établies ; `publication_date=unknown`, statut documentaire `blocked` pour les conclusions requérant la date.
- Statut : **open**. Conserver l'original et les dates concurrentes ; rechercher un erratum ou une confirmation datée du partenaire. Décision humaine : en attente.

