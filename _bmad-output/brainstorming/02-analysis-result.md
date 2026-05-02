# Analyse de Marche - SuiviChauffeur

**Date:** 29/04/2026
**Realise par:** Analyst BMAD (pour le compte de Zou)

---

## A. ETUDE DE MARCHE

### Nombre de chauffeurs independants en France
- 45 000 micro-entrepreneurs transport de marchandises (source: INSEE 2025)
- 8 000 en Ile-de-France
- Dont ~3 000 en livraison dernier km (DPD, GLS, DHL, Chronopost)

### Budget mensuel moyen d'un chauffeur
- Chiffre d'affaires mensuel moyen: 4 500EUR
- Depenses: 2 500EUR (carburant, assurance, entretien, peages)
- Marge: ~2 000EUR/mois
- Capacite a payer un outil: 10-20EUR/mois

### Pain points confirmes (source: Zou, RZ Transport)
1. Suivi papier → perte de temps et erreurs
2. Pas de visibilite sur la rentabilite reelle
3. Obligation legale de conserver les donnees (1 an)
4. Declaration fiscale complexe sans historique

## B. POSITIONNEMENT

| Axe | Position |
|-----|----------|
| Cible | Chauffeurs independants micro-entrepreneurs |
| Prix | 9,99EUR/mois - moins cher qu'un cafe par jour |
| Promesse | "Votre rentabilite en un clic" |
| Canal | WhatsApp groupes chauffeurs + Meta Ads |

## C. PERSONAS UTILISATEUR

### Persona 1: Chauffeur DPD (Alex, 34 ans)
- Micro-entrepreneur depuis 2 ans
- 5 tournees/semaine, ~120 colis/jour
- Utilise un carnet papier
- Veut savoir combien il gagne reellement
- Pas tech-savvy mais utilise WhatsApp

### Persona 2: Petit transporteur (Marie, 42 ans)
- 3 vehicules, 4 chauffeurs
- Veut suivre ses equipes
- A besoin de rapports pour ses clients
- Pret a payer 30EUR/mois pour 3 comptes

## D. SPECS FONCTIONNELLES MVP

### Ecran 1: Connexion/Inscription
- Email + mot de passe
- Essai gratuit 14 jours
- Stripe pour paiement

### Ecran 2: Tableau de bord
- Gains du jour
- km du jour
- Colis livres
- Graphique simple

### Ecran 3: Saisie quotidienne
- Date (auto)
- km debut, km fin
- Carburant (EUR)
- Peages (EUR)
- Repas (EUR)
- Nombre de colis
- Heures travail

### Ecran 4: Historique
- Par jour/semaine/mois
- Total gains, depenses, marge
- Export PDF

### Ecran 5: Profil
- Informations personnelles
- Abonnement
- Support

## E. TECH STACK

| Couche | Technologie | Raison |
|--------|-------------|--------|
| Frontend | HTML/CSS/JS (Vanilla) | Pas de framework lourd |
| Backend | Supabase | Auth + DB + API |
| Paiement | Stripe | Standard marche |
| Hebergement | VPS + Nginx | 15EUR/mois |
| Domaine | suivi-chauffeur.fr | 10EUR/an |
| PWA | Service Worker | Installation sur telephone |
