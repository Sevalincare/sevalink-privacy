# SevaLink Privacy Policy Website

A clean, professional privacy policy website for the SevaLink platform, hosted on Vercel. Covers both the **SevaLink User App** and **SevaLink Driver App**.

## 🔗 Live URLs (once deployed)

| Page | URL |
|------|-----|
| Home (Policy Selector) | `https://privacy.sevalink.in` |
| SevaLink User App Policy | `https://privacy.sevalink.in/app` |
| SevaLink Driver App Policy | `https://privacy.sevalink.in/driver` |

> Update the domain above once you configure it in the Vercel dashboard.

## 📁 Project Structure

```
sevalink-privacy/
├── index.html          # Landing page — links to both policies
├── app-privacy.html    # Privacy Policy for SevaLink User App
├── driver-privacy.html # Privacy Policy for SevaLink Driver App
├── styles.css          # Global stylesheet (shared across all pages)
├── vercel.json         # Vercel deployment configuration
└── README.md           # This file
```

## 🚀 Deploying to Vercel

### Option 1: Vercel CLI (Recommended)

```bash
# Install Vercel CLI (if not installed)
npm install -g vercel

# From the sevalink-privacy directory
cd sevalink-privacy
vercel

# For production deployment
vercel --prod
```

### Option 2: Vercel Dashboard (GitHub Integration)

1. Push this folder to a new GitHub repository (e.g., `sevalink-privacy`).
2. Go to [vercel.com/new](https://vercel.com/new).
3. Import the repository.
4. Framework preset: **Other** (no build step required).
5. Root directory: `/` (already correct since it's a static site).
6. Click **Deploy**.

### Custom Domain (Google Play Store requirement)

1. In Vercel Dashboard → Project → Settings → Domains.
2. Add `privacy.sevalink.in` (or `sevalink.in/privacy` if you prefer a path).
3. Add the required DNS records (CNAME/A record) in your domain registrar.
4. SSL is automatically provisioned by Vercel.

## 📋 Policy Coverage

### SevaLink User App (`/app`)
- Data collected: Profile, location (foreground only), health notes, payment info
- Key sections: DPDPA 2023 compliance, health data handling, Cashfree payments
- Effective Date: April 24, 2025

### SevaLink Driver App (`/driver`)
- Data collected: KYC documents, background location, earnings, performance metrics
- Key sections: Background location transparency, KYC document retention, financial data
- Effective Date: April 24, 2025

## 🛡️ Security Headers

The `vercel.json` configures the following security headers on all pages:
- `X-Content-Type-Options: nosniff`
- `X-Frame-Options: DENY`
- `X-XSS-Protection: 1; mode=block`
- `Strict-Transport-Security` (HSTS with preload)
- `Referrer-Policy: strict-origin-when-cross-origin`
- `Permissions-Policy` (blocks camera/mic/geolocation from iframe embedding)

## ✏️ Updating Policies

1. Edit `app-privacy.html` for User App policy changes.
2. Edit `driver-privacy.html` for Driver App policy changes.
3. Update the `Effective Date` / `Last Updated` meta pills in the hero section.
4. Push to GitHub — Vercel auto-deploys on every push to `main`.

## 📬 Contact

For privacy-related questions: **privacy@sevalink.in**

---

© 2025 SevaLink Technologies Pvt. Ltd.
