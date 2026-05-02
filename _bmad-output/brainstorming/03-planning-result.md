# Plan de Projet - SuiviChauffeur

**Duree:** 4 semaines (MVP)
**Budget:** 390EUR

---

## Semaine 1: Foundation (Setup)
- [x] S1.1: Nom de domaine suivi-chauffeur.fr (10EUR)
- [x] S1.2: Hebergement VPS + Nginx
- [x] S1.3: Compte Supabase (projet + tables)
- [x] S1.4: Compte Stripe (test mode)
- [x] S1.5: Repository Git + structure projet

## Semaine 2: Core Features
- [ ] S2.1: Page d'accueil + inscription/connexion
- [ ] S2.2: Formulaire saisie quotidienne
- [ ] S2.3: Calcul automatique des gains
- [ ] S2.4: Tableau de bord avec graphiques
- [ ] S2.5: Historique et filtres

## Semaine 3: Finalisation MVP
- [ ] S3.1: Export PDF
- [ ] S3.2: PWA (installation sur telephone)
- [ ] S3.3: Mode hors-ligne
- [ ] S3.4: Integration Stripe paiement
- [ ] S3.5: Period d'essai 14 jours

## Semaine 4: Tests & Lancement
- [ ] S4.1: Tests utilisateurs (5 chauffeurs RZ Transport)
- [ ] S4.2: Corrections bugs
- [ ] S4.3: Page de destination + landing
- [ ] S4.4: Campagne Meta Ads (200EUR)
- [ ] S4.5: Lancement officiel

## STRUCTURE BASE DE DONNEES

`sql
-- Table: utilisateurs (via Supabase Auth)
-- Table: saisies_quotidiennes
CREATE TABLE saisies (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES auth.users,
  date DATE NOT NULL DEFAULT CURRENT_DATE,
  km_debut INTEGER,
  km_fin INTEGER,
  carburant DECIMAL(10,2),
  peages DECIMAL(10,2),
  repas DECIMAL(10,2),
  colis_livres INTEGER,
  heures_travail DECIMAL(4,1),
  total_gains DECIMAL(10,2),
  total_depenses DECIMAL(10,2),
  marge DECIMAL(10,2),
  created_at TIMESTAMP DEFAULT NOW()
);

-- Table: abonnements
CREATE TABLE abonnements (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES auth.users,
  stripe_customer_id TEXT,
  stripe_subscription_id TEXT,
  statut TEXT DEFAULT 'essai',
  date_fin_essai DATE,
  created_at TIMESTAMP DEFAULT NOW()
);
`

## PRIX DE REVIENT

| Mois | Utilisateurs | Serveur | Stripe | Total | Revenu (9,99EUR) |
|:----:|:------------:|:-------:|:-----:|:-----:|:----------------:|
| M1 | 5 | 15EUR | 1,5EUR | 16,5EUR | 50EUR |
| M3 | 15 | 15EUR | 4,5EUR | 19,5EUR | 150EUR |
| M6 | 30 | 15EUR | 9EUR | 24EUR | 300EUR |
| M12 | 100 | 30EUR | 30EUR | 60EUR | 1000EUR |
