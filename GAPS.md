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

## Lacunes ouvertes au 2026-09-27

- GAP-20260927-veolia-2025-annual-report — Rôle 1 (scope & evidence) / Rôle 2 (analyse) — Le Document d'enregistrement universel 2025 de Veolia (résultats FY2025 publiés février 2026, chiffres GreenUp) n'est pas encore dans `raw/`. Nécessaire pour sourcer EBITDA, levier, ROCE et indicateurs GreenUp cités dans le briefing sans dépendre du PDF pédagogique. Piste : veolia.com, espace investisseurs, résultats annuels 2025. Statut : open.
- GAP-20260927-veolia-debt-maturity — Rôle 3 (capacité financière, "the hard one") — Profil de maturité de la dette, définition du levier retenue par Veolia (net financial debt / EBITDA), et le point à fin juin 2026 (24 548 M€ cité dans le briefing) ne sont pas sourcés à la publication primaire. Piste : rapport semestriel S1 2026, présentation dette investisseurs. Statut : open.
- GAP-20260927-rating-reports — Rôle 3 — Rapports d'agence (Moody's Baa1, S&P/Fitch BBB) sur Veolia : déclencheurs de dégradation, seuils de levier publiés. Accès potentiellement restreint (abonnement) : documenter si seule une page web ou un communiqué de presse est accessible. Statut : open.
- GAP-20260927-water-technologies-clean-earth — Rôle 1 / Rôle 4 (coût et économie) — Documents de transaction (communiqués, multiples, synergies) pour le rachat des 30 % de Water Technologies (CDPQ) et l'acquisition Clean Earth (cédée par Enviri Corporation, NYSE). Le dépôt SEC d'Enviri (10-K / segment Clean Earth) est la source la plus solide avant que l'actif ne disparaisse dans le reporting Veolia. Statut : open.
- GAP-20260927-comparables — Rôle 2 (benchmark) — Comparables cotés pour les trois boosters : eau industrielle, déchets dangereux (Clean Harbors en particulier), bioénergie/efficacité énergétique. Statut : open.
- GAP-20260927-bioenergy-regulation — Rôle 5 (règles et contraintes) — Cadre réglementaire biométhane/biomasse/RED III (UE) et dispositifs français (CSRD pour la double matérialité, réglementation déchets dangereux). Statut : open.
- GAP-20260927-tuck-ins-2025 — Rôle 1 — Les trois petites acquisitions annoncées le 26 juin 2025 (New England Disposal Technologies, New England MedWaste, Ingenium) n'ont pas de prix public ; le briefing le signale explicitement. Ne pas inventer de valeur : consigner "prix non public" si aucune source primaire ne le publie. Statut : open (attendu wont_fill si confirmé non public).
