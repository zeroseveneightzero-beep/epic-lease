# EPIC LEASE — Android-first Command Center

This is the first real tablet UI for the Mandaluyong AI Leasing system. It authenticates with Supabase and reads the production tables created in the database setup.

## Supabase configuration

1. Open Supabase Dashboard → Settings → API Keys.
2. Create/copy the **Publishable key** (`sb_publishable_...`).
3. Put it in `config.js` as `publishableKey`.
4. Never put a Secret/service_role key in this file.

The browser client is protected by Supabase Auth + Row Level Security.

## Run locally

Because this is a static PWA, any static server works. Example:

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080`.

## Deploy

Upload this folder to a static host such as Cloudflare Pages. After deployment, open the URL on Android Chrome and choose **Add to Home screen** / **Install app** when offered.

## Current scope

- Supabase authentication
- Live counts from leads/properties/tenants/matches/tasks
- Human approval queue
- Recent tasks
- Lead/property/tenant/match/task views
- AI workforce status board
- PWA manifest
- Service worker shell

Not yet connected: live source adapters, AI enrichment workers, matching automation, outbound messaging, and production 24/7 orchestration.
