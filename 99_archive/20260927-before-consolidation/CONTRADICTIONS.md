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
