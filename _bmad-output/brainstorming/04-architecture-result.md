# Architecture Technique - SuiviChauffeur

## Vue d'ensemble
`
[Client PWA] ←→ [Supabase API] ←→ [VPS Nginx]
       ↓                                  ↓
[Service Worker]                  [Stripe Webhook]
       ↓
[IndexedDB (offline)]
`

## Stack retenu
- **Frontend:** HTML/CSS/JS pur + PWA
- **Backend:** Supabase (auth, DB, API REST)
- **Paiement:** Stripe Elements + Webhook
- **Hebergement:** VPS Hostinger + Nginx reverse proxy
- **Domaine:** suivi-chauffeur.fr

## Pages
1. / - Landing page
2. /app - Application (PWA)
   - /app/dashboard - Tableau de bord
   - /app/saisie - Formulaire de saisie
   - /app/historique - Historique + export
   - /app/profil - Profil utilisateur

## Securite
- Auth via Supabase (email + mot de passe)
- Row Level Security (RLS) sur les donnees
- HTTPS partout (certbot)
- Donnees isolees par utilisateur

## Performance
- PWA avec cache offline
- IndexedDB pour le mode hors-ligne
- CDN pour les assets statiques
- Chargement differe des graphiques
