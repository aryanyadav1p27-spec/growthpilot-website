# GrowthPilot OS

GrowthPilot OS — Public Website, Client Portal, and Client Workspace Management.

## Website
- Main entry point: `index.html`
- Static, responsive landing page with client sign-in/sign-up UI.
- Supabase Auth uses the public publishable key in the browser. Never put a Supabase service-role key or other secret in this repository.
- Client project records are not displayed by this starter page; secure data access requires verified authentication and database row-level security policies.

## Cloudflare Pages
This repository can be deployed as a static site from the `main` branch when a Cloudflare Pages project is connected to this repository.
- Framework preset: None
- Build command: leave empty
- Build output directory: `/`
- Production branch: `main`

A GitHub push triggers a Cloudflare Pages deployment only if the Cloudflare Pages project is already connected and configured for this repository. Verify the deployment result in Cloudflare Dashboard → Workers & Pages → your Pages project → Deployments.
