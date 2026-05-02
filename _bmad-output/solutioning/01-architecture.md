# Architecture Technique - SuiviChauffeur v1.0

## Decision: Static PWA sans backend
Justification: MVP, budget 500EUR, pas de besoin temps reel
Evolution future: Supabase quand nombre d'utilisateurs > 50

## Stack
- Frontend: HTML/CSS/JS vanilla
- Framework CSS: Tailwind CDN
- Persistance: localStorage (plus tard Supabase)
- PWA: Service Worker + manifest
- Hebergement: Netlify (gratuit)

## Structure fichiers
`
suivi-chauffeur/
├── src/
│   ├── index.html      (app complete monopage)
│   ├── config.json     (configuration)
├── public/
│   ├── manifest.json   (PWA)
│   ├── nginx.conf      (deploiement)
├── _bmad/              (BMAD Method)
├── _bmad-output/       (artefacts)
`

## Data model (localStorage)
`json
{
  "users": [{"id","name","email","pass","phone","company"}],
  "entries": [{"id","date","kmDebut","kmFin","km","carburant","peages","repas","colis","heures","gain","dep","marge"}]
}
`

## RLS (futur Supabase)
- Chaque utilisateur voit ses propres donnees
- Row Level Security par user_id
