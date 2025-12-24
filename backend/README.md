# Dossier Backend

Ce dossier contient tous les services backend : Supabase et n8n.

## Structure

```
backend/
├── supabase/
│   ├── migrations/     # Migrations de schéma SQL
│   ├── functions/      # Edge Functions Supabase
│   └── seed.sql        # Données initiales
└── n8n-workflows/
    ├── analytics.json  # Workflow analytics
    └── events.json     # Workflow events
```

## Supabase Setup

```bash
cd backend/supabase
supabase init
supabase db push
```

## Configuration

Variables d'environnement requises :
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`
- `SUPABASE_SERVICE_ROLE_KEY`

Voir [docs/SETUP.md](../docs/SETUP.md) pour détails.
