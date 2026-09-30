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


## Standalone Client Ops (Supabase-hosted)

- App URL: https://phtuvjriwztridhonqep.supabase.co/functions/v1/client-ops-web
- Downloadable HTML source: https://github.com/aryanyadav1p27-spec/growthpilot-website/blob/client-ops-standalone/index.html?raw=1
- The app uses Supabase Auth and the `client-operations` Edge Function. Do not add a service-role key to browser code.
- The Website Studio can register a hostname, generate a client-facing `index.html`, run a basic public HTML audit, and prepare (but not automatically send) client outreach drafts.
- A client website must be deployed at the same hostname registered in Website Studio for its enquiry form to submit to the matching form record.

### Optional Cloudflare Pages deployment

Create a separate Cloudflare Pages project from this repository using branch `client-ops-standalone`, build command empty, and build output directory `/`. Do not connect this branch to the existing production Worker unless you intend to replace that Worker. The Supabase-hosted app URL above can be used without Cloudflare deployment.
