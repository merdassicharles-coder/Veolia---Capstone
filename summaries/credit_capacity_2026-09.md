---
doc_id: credit_capacity_2026-09
title: Notation de crédit, dette nette et capacité financière Veolia (résumé groupé)
issuer: Veolia Environnement ; Moody's ; S&P Global Ratings ; Fitch Ratings
doc_type: credit_bundle
period: 2024-2026
currency: EUR
default_unit: M€
retrieved: 2026-09-27
collected_by: Claude (Cowork), agent Source — Crédit & capacité
source_ids:
  - SRC-credit-20260927-moodys-credit-opinion
  - SRC-credit-20260927-sp-affirmation
  - SRC-credit-20260927-fitch-withdrawal
  - SRC-credit-20260927-debt-ratings-page
  - SRC-credit-20260927-disposal-program
notes: Résumé groupé. Le Credit Opinion Moody's (PDF republié par Veolia) et les communiqués de résultats FY2025/H1 2026 sont des PDF officiels réels sur veolia.com, non téléchargés physiquement (réseau restreint). Rapports complets d'agences (RatingsDirect S&P, etc.) non consultés — accès abonnement.
---

# Crédit et capacité financière — le workstream « the hard one »

## En bref
Correction importante par rapport au briefing interne : **Fitch ne note plus Veolia depuis le 12 juin 2024** (retrait pour raisons commerciales) — Veolia n'est donc suivie que par deux agences (Moody's Baa1 stable, S&P BBB stable), pas trois. Les deux chiffres de dette nette cités dans le briefing (20 764 M€ au 30/06/2025 et 24 548 M€ au 30/06/2026) sont confirmés mot pour mot par le communiqué officiel Veolia H1 2026. L'objectif de levier ≤3x en 2027 est confirmé textuellement par Veolia elle-même.

## Chiffres clés

| Donnée | Valeur | Date | Source | Fiabilité |
|---|---|---|---|---|
| Notation Moody's | Baa1, perspective stable | Confirmation 04/05/2026 ; Credit Opinion 02/12/2025 | SRC-credit-20260927-moodys-credit-opinion | [Credit Opinion (PDF, republié par Veolia)](https://www.veolia.com/sites/g/files/dvc4206/files/document/2025/12/Credit_Opinion_Veolia-Environnement-2Dec2025.pdf) |
| Seuil dégradation Moody's | FFO/dette nette < ~17-19% | 02/12/2025 | idem | idem |
| FFO/dette nette observé | 19,0% (LTM juin 2025) vs 21,3% (2024) | 02/12/2025 | idem | idem |
| Notation S&P | BBB, perspective stable | Action 09/01/2026 | SRC-credit-20260927-sp-affirmation | [Cbonds](https://cbonds.com/news/3743215/) — secondaire, seuils/méthodologie non publics |
| **Notation Fitch : RETIRÉE** | Dernier niveau avant retrait : BBB stable | Retrait effectif 12/06/2024 | SRC-credit-20260927-fitch-withdrawal | [MarketScreener](https://www.marketscreener.com/quote/stock/VEOLIA-ENVIRONNEMENT-4726/news/Fitch-Affirms-Withdraws-Veolia-Environnement-Ratings-46954545/) — **corrige l'hypothèse du briefing interne (3 agences → 2 agences actives)** |
| Dette financière nette | 17 819 M€ (fin 2024) → 19 657 M€ (fin 2025) | FY2024/FY2025 | Communiqué FY2025 (PDF officiel) | Officiel Veolia |
| Dette financière nette | **20 764 M€** | 30/06/2025 | Communiqué H1 2026 (PDF officiel) | Officiel Veolia — confirme le briefing interne |
| Dette financière nette | **24 548 M€** | 30/06/2026 | idem | Officiel Veolia — confirme le briefing interne ; hausse ≈+3,8 Md€ due à Clean Earth (2 778 M€) et Enviropacific (137 M€) |
| Objectif levier 2027 | ≤ 3x | Guidance | Investor Presentation Clean Earth (PDF officiel, nov. 2025) | Officiel Veolia |
| Dette ajustée Moody's | 26,4 Md€ (juin 2025), pic ~29 Md€ (2026), reflux 2027 | Prospectif | Credit Opinion Moody's | Officiel Veolia (repost Moody's) — ne pas confondre avec la dette financière nette publiée |
| Liquidité | 8,9 Md€ cash + 6,3 Md€ lignes non tirées | Juin 2025 | idem | idem |
| Programme de cessions lié à Clean Earth | >2 Md€ sur 2 ans (échéance ~mi-2028) | Nov. 2025, actualisé juil. 2026 | SRC-credit-20260927-disposal-program | Investor Presentation Clean Earth + PR H1 2026 |
| Cessions déjà signées | ~500 M€ | Fin juin 2026 | idem | Officiel Veolia |

## Points importants
- **Corriger le modèle** : utiliser uniquement Moody's (Baa1) et S&P (BBB) comme contraintes de notation — Fitch n'est plus active depuis juin 2024.
- Les deux chiffres-clés de dette du briefing interne sont validés à l'euro près — base solide pour le workstream capacité financière.
- La dette "ajustée agence" (Moody's, avec retraitements hybrides/leases) diffère de la dette financière nette publiée par Veolia — à ne pas confondre dans le modèle de capacité.
- Le programme de cessions (>2 Md€, dont 500 M€ déjà signés) est la variable de désendettement identifiable à utiliser dans le modèle de capacité.

## Limites de l'extraction
- **Profil de maturité de la dette (échéancier par année) : non trouvé publiquement** — à marquer "unknown" dans le modèle plutôt que d'estimer. Nécessiterait un traitement fichier par fichier des prospectus, non réalisable dans cet environnement.
- Détail méthodologique des seuils de dégradation S&P : non public (rapport complet sous abonnement).
- Les documents PDF officiels cités (Credit Opinion, communiqués FY2025/H1 2026, Investor Presentation Clean Earth) n'ont pas été téléchargés physiquement dans `raw/` — à faire manuellement pour passer en statut "verified".
