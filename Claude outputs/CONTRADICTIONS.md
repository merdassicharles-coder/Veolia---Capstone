# Registre des contradictions

Ajouter une section par divergence ; ne pas effacer les décisions antérieures. Statuts : open, investigating, proposed_resolution, resolved (validation humaine uniquement).

## Modèle à copier
- contradiction_id : CON-YYYYMMDD-<slug>
- Objet / indicateur :
- Preuve A : valeur, unité, devise, période, périmètre ; source_id + document + page PDF + date de publication
- Preuve B : valeur, unité, devise, période, périmètre ; source_id + document + page PDF + date de publication
- Écart et impact sur l'analyse / les modèles :
- Explications possibles (hypothèses, pas conclusions) :
- Vérifications réalisées / à faire :
- Statut : open
- Détecté par / date / branche ou PR :
- Proposition de traitement :
- Décision humaine, justification, validateur et date :
- Historique des changements :

## CON-20260927-dechets-dangereux-cible-2027

- **Objet / indicateur** : cible GreenUp 2027 de tonnage de déchets dangereux et polluants traités.
- **Preuve A** : **9 Mt** en 2027 ; source = briefing pédagogique EDHEC (SRC-setup-20260927-capstone-brief), page PDF non précisée dans le corps du slide, date de publication du briefing inconnue (fichier non daté officiellement).
- **Preuve B** : **10 Mt** en 2027 ; sources = SRC-veolia-20260927-greenup-launch (communiqué GreenUp, Veolia Belgique, ~28/02-06/03/2024) et SRC-veolia-20260927-greenup-strategic-page (page corporate officielle Veolia, non datée) — deux sources Veolia indépendantes convergent sur 10 Mt.
- **Écart et impact** : 1 Mt d'écart (+11%) sur un indicateur central du rôle 2 (analyse cœur) et du rôle 1 (scope). Change la base de calcul de l'écart stratégique 2027 si le mauvais chiffre est utilisé.
- **Explications possibles** : le briefing pédagogique a pu arrondir, se référer à une version antérieure de la cible GreenUp (le programme a pu être ajusté depuis son lancement), ou contenir une erreur de transcription. Les deux sources Veolia consultées sont plus récentes/directement officielles que le briefing pédagogique.
- **Vérifications réalisées** : recoupement de deux pages Veolia indépendantes (communiqué de lancement + page corporate), toutes deux affichant 10 Mt. Aucune version antérieure du communiqué GreenUp avec un chiffre à 9 Mt n'a été recherchée spécifiquement.
- **Statut** : open.
- **Détecté par / date** : Claude (Cowork), agent Source Veolia, 2026-09-27, branche agent/setup-data-room.
- **Proposition de traitement** : utiliser 10 Mt comme référence (sources Veolia officielles, plus récentes) mais signaler explicitement l'écart avec le briefing pédagogique dans le rapport final, sans le corriger silencieusement. Chercher si une version antérieure du plan GreenUp (2023) mentionnait 9 Mt, ce qui expliquerait un chiffre daté dans le briefing.
- **Décision humaine, justification, validateur et date** : en attente.

## CON-20260927-fitch-rating

- **Objet / indicateur** : nombre et identité des agences de notation suivant Veolia (contrainte du workstream capacité financière, rôle 3).
- **Preuve A** : le briefing pédagogique (SRC-setup-20260927-capstone-brief) mentionne une notation Moody's Baa1 et une notation "S&P/Fitch BBB", implicitement 3 agences actives.
- **Preuve B** : SRC-credit-20260927-fitch-withdrawal (MarketScreener, 12/06/2024) indique que **Fitch a retiré sa notation de Veolia pour raisons commerciales** ; corroboré par l'absence totale de Fitch sur SRC-credit-20260927-debt-ratings-page (page officielle Veolia "Debt & ratings", consultée 2026-09-27) qui ne liste que Moody's et S&P.
- **Écart et impact** : le modèle de capacité financière (rôle 3) ne doit contraindre que sur 2 agences actives (Moody's Baa1, S&P BBB), pas 3. Un modèle qui suppose une contrainte Fitch active serait fondé sur une donnée obsolète depuis juin 2024.
- **Explications possibles** : le briefing pédagogique a pu être rédigé ou basé sur une source antérieure à juin 2024, ou reprendre une convention de langage générique "Moody's/S&P/Fitch" sans vérification à jour pour cet émetteur précis.
- **Vérifications réalisées** : recoupement de deux sources indépendantes (article de presse spécialisée + page officielle Veolia sans mention Fitch).
- **Statut** : open.
- **Détecté par / date** : Claude (Cowork), agent Source Crédit & capacité, 2026-09-27, branche agent/setup-data-room.
- **Proposition de traitement** : utiliser explicitement 2 agences actives (Moody's, S&P) dans le modèle et le rapport, en mentionnant le retrait Fitch (2024) comme point factuel plutôt que de l'ignorer silencieusement.
- **Décision humaine, justification, validateur et date** : en attente.

## CON-20260927-ca-energie-2023-base

- **Objet / indicateur** : chiffre d'affaires "énergie" 2023 de Veolia servant de base au calcul de la trajectoire du booster bioénergie GreenUp.
- **Preuve A** : **12 Md€** ; source = page corporate Veolia (SRC-bioenergy-20260927-near-me-greenup-page, near-middle-east.veolia.com), non datée précisément.
- **Preuve B** : **>10 Md€** ("over €10 Billion of its business already linked to energy") ; source = communiqué officiel Businesswire du 11/01/2024 (SRC-bioenergy-20260927-4bn-investment-announcement).
- **Preuve C** : **12,3 Md€** ("2023 Energy revenues: €12.3bn total") ; source = PDF du Capital Markets Day GreenUp du 29/02/2024 (SRC-bioenergy-20260927-greenup-cmd-feb2024) — mais ce total inclut explicitement l'eau et les déchets liés à l'énergie, pas seulement la bioénergie, donc n'est pas nécessairement incompatible avec les deux autres chiffres si leur périmètre diffère aussi.
- **Écart et impact** : jusqu'à 2,3 Md€ d'écart selon la source retenue (soit ~20%) sur un chiffre de base utilisé pour calculer la trajectoire de croissance du booster bioénergie (rôle 1 et rôle 2). Le sous-chiffre "bioénergie seule" dérivé du PDF CMD (~615 M€ en 2023, objectif combiné 4,9 Md€ en 2030) provient d'une extraction automatisée non relue ligne à ligne et n'a pas pu être recoupé indépendamment.
- **Explications possibles** : les trois chiffres pourraient couvrir des périmètres légèrement différents ("énergie" au sens large vs "énergie déjà liée au groupe" vs total incluant eau/déchets) plutôt que d'être strictement contradictoires ; ou bien une communication moins précise sur la page corporate (12 Md€, arrondi) par rapport aux deux communications officielles plus formelles (Businesswire, CMD).
- **Vérifications réalisées** : recoupement des trois sources par un agent de recherche dédié ; aucune lecture manuelle ligne par ligne du PDF CMD (72+ slides) n'a été effectuée pour confirmer le sous-chiffre bioénergie de 615 M€.
- **Statut** : open.
- **Détecté par / date** : Claude (Cowork), agent de recherche bioénergie n°1, 2026-09-27, branche agent/setup-data-room.
- **Proposition de traitement** : pour le CA énergie total 2023, utiliser le chiffre du communiqué officiel Businesswire (>10 Md€) ou du PDF CMD (12,3 Md€, en précisant le périmètre élargi eau+déchets), en évitant le chiffre de la page corporate moins formel (12 Md€) sauf clarification. Pour le sous-segment bioénergie seul (~615 M€ / objectif 4,9 Md€), ne pas citer sans relecture manuelle directe du PDF CMD.
- **Décision humaine, justification, validateur et date** : en attente.

## CON-20260927-valenton-capacite

- **Objet / indicateur** : capacité annuelle de production/injection de biométhane de l'unité de Valenton (SIAAP, Val-de-Marne, France).
- **Preuve A** : **45 GWh/an** (injection annuelle prévue à partir de 2025) ; source = article Environnement Magazine du 31/10/2024, relayant l'inauguration officielle du 29/10/2024 (SRC-bioenergy-20260927-valenton-biomethane-siaap).
- **Preuve B** : **163 GWh** ; source = PDF du Capital Markets Day GreenUp du 29/02/2024 (SRC-bioenergy-20260927-greenup-cmd-feb2024), cité comme exemple de site bioénergie.
- **Écart et impact** : facteur ~3,6x entre les deux chiffres pour le même site — écart trop important pour être une simple imprécision d'arrondi. Impact limité sur la trajectoire globale du booster (Valenton n'est qu'un exemple de site parmi d'autres) mais pertinent si ce site est utilisé comme illustration chiffrée dans le mémoire.
- **Explications possibles** : le chiffre du CMD (février 2024, avant l'inauguration d'octobre 2024) pourrait correspondre à une capacité de traitement biogaz totale ou à une projection différente (capacité nominale maximale vs injection réseau réelle prévue) ; le chiffre de l'article de presse (45 GWh/an) semble plus fiable car publié après l'inauguration effective et correspond à un objectif d'injection concret ; une confusion d'unité ou de site dans l'extraction automatisée du PDF CMD n'est pas exclue.
- **Vérifications réalisées** : le communiqué SIAAP original n'a pas pu être consulté (erreur 403) pour arbitrer entre les deux chiffres ; aucune troisième source trouvée.
- **Statut** : open.
- **Détecté par / date** : Claude (Cowork), agent de recherche bioénergie n°1, 2026-09-27, branche agent/setup-data-room.
- **Proposition de traitement** : privilégier le chiffre de 45 GWh/an (article de presse post-inauguration, plus récent et plus spécifique) pour toute citation dans le mémoire, en signalant l'écart avec le PDF CMD plutôt que de le corriger silencieusement. Tenter d'obtenir le communiqué SIAAP original (siaap.fr) pour trancher définitivement.
- **Décision humaine, justification, validateur et date** : en attente.
