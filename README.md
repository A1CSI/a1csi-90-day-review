# A-1 Certified Service — 90-Day Technician Progress App

Ready for GitHub + Cloudflare Pages.

## Deploy
1. Create a GitHub repository such as `a1csi-90-day-review`.
2. Upload this repository exactly as packaged.
3. In Cloudflare go to **Workers & Pages → Create → Pages → Connect to Git**.
4. Select the GitHub repository.
5. Set Production branch to `main`, Framework preset to `None`, Build command to `exit 0`, and Build output directory to `public`.
6. Deploy.

## Email setup
The Pages Function sends the completed report to `mthomas@a1csi.com` using Resend.

1. Create a Resend account and verify a sending domain you control.
2. Create a Resend API key.
3. In the Cloudflare Pages project go to **Settings → Variables and Secrets**.
4. Add `RESEND_API_KEY` as a secret.
5. Add `FROM_EMAIL`, for example `A-1 Technician Reports <reports@a1csi.com>`, using an address on the verified sending domain.
6. Redeploy.

## iPad use
Open the Cloudflare Pages HTTPS URL in Chrome. Do not open `index.html` from Apple Files.

## Optional custom URL
Attach a custom domain such as `techreview.a1csi.com` in the Cloudflare Pages project.
