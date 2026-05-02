# Session de Brainstorming - SuiviChauffeur

**Date:** 29/04/2026
**Participant:** Tiana (Zou) - Gerant RZ GROUPE
**Projet:** Micro-SaaS pour chauffeurs-livreurs independants
**Budget:** 500 EUR

---

## 1. LE PROBLEME

En tant que gerant de RZ TRANSPORT, je vois tous les jours:
- 35 chauffeurs qui notent leurs infos sur des carnets papier
- Des erreurs de saisie, des feuilles perdues
- Aucun outil simple et abordable pour les independants
- Les chauffeurs DPD/GLS/DHL n'ont pas de solution pour suivre leur rentabilite
- Excel c'est trop complexe, les apps pro coutent 50-100EUR/mois

## 2. LA SOLUTION

**SuiviChauffeur** - Une app mobile-first qui permet:
- Suivi quotidien: km parcourus, colis livres, heures travaillees
- Calcul automatique: gains, depenses, marge journaliere
- Generation de rapports hebdomadaires
- Export PDF pour declaration

## 3. MARCHE CIBLE

- Chauffeurs independants (micro-entrepreneurs)
- Livreurs DPD / GLS / DHL en IDF
- Petits transporteurs (1-5 vehicules)
- Estimation: 500+ chauffeurs rien que sur Paris

## 4. CONCURRENCE

| Concurrent | Prix | Forces | Faiblesses |
|------------|:----:|--------|------------|
| Everlance | 8EUR/mois | Automatique trajet | Pas adapte transport |
| Roadie | Gratuit | Simple | Pas de stats |
| Excel/Google Sheets | Gratuit | Flexible | Chronophage |
| **SuiviChauffeur** | **9,99EUR** | **Metier transport** | **Nouveau** |

## 5. BUSINESS MODEL

- Abonnement mensuel: 9,99EUR TTC
- Pas de commission sur les gains (contrairement aux concurrents)
- Perioode d'essai gratuite 14 jours
- Objectif M1: 5 clients (50EUR)
- Objectif M6: 30 clients (300EUR/mois)
- Objectif M12: 100 clients (1000EUR/mois)

## 6. MVP (Minimum Viable Product)

- Inscription avec email
- Saisie quotidienne: km debut/fin, carburant, colis, heures
- Tableau de bord avec gains journaliers
- Historique par mois
- Export PDF
- Application mobile-first (PWA)

## 7. BUDGET 500EUR

| Poste | Cout | Details |
|------|:----:|---------|
| Domaine | 10EUR | suivi-chauffeur.fr |
| VPS | 180EUR | 1 an chez Hostinger |
| Supabase | 0EUR | Tier gratuit |
| Stripe | 0EUR | Sans abonnement |
| Design | 0EUR | Tailwind CSS gratuit |
| Marketing | 200EUR | Meta Ads cible chauffeurs |
| Imprevus | 110EUR | Marge de securite |
| **TOTAL** | **390EUR** | **Restant: 110EUR** |

## 8. RISQUES

- Adoption lente → Strategy: bouche-a-oreille via les groupes WhatsApp chauffeurs
- Concurrence → Avantage: expertise metier, fonctionnalites ciblees
- Churn → Fidelisation: rapport hebdo personnalise envoye par email
- Technique → Stack simple (Supabase + HTML/JS) pas de risque majeur
