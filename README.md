# V-Check Landing (Render)

This repo deploys the V-Check landing page to Render Static Site.

## Structure
- `site/index.html`: landing page
- `site/vcheck_sample_report_dark.html`: sample report page
- `render.yaml`: Render Blueprint config

## Deploy
Use Render Blueprint with this repository:
- Render dashboard -> New -> Blueprint
- Select this repo
- Create service

Recommended Render settings:
- Branch: `main`
- Root Directory: `deploy/render-site`
- Static Publish Path: `./site`

## Local Sync
From project root:
```bash
./scripts/sync_landing_files.sh
./scripts/verify_landing_consistency.sh
```

After Render deploy:
```bash
./scripts/smoke_check_live_landing.sh https://vcheck-landing.onrender.com
```
