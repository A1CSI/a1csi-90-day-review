# Cloudflare Pages deployment

## GitHub repository must contain these items at the TOP LEVEL

- .gitignore
- README.md
- DEPLOYMENT.md
- wrangler.toml
- functions/
- public/

Do NOT upload the ZIP file itself as the only file in GitHub. Extract it first, then upload the files/folders above.

## Cloudflare Pages settings

1. Workers & Pages > Create > Pages > Connect to Git.
2. Choose the GitHub repository.
3. Production branch: main
4. Framework preset: None
5. Build command: exit 0
6. Build output directory: public
7. Root directory: leave blank
8. Save and deploy.

The included wrangler.toml also declares ./public as the Pages output directory.

## Email settings after first successful deployment

Cloudflare project > Settings > Variables and Secrets:
- RESEND_API_KEY = your Resend API key
- FROM_EMAIL = a verified sender such as A-1 Technician Reports <reports@a1csi.com>

Redeploy after saving the variables.
