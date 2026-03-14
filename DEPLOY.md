# SteppeIn Website Deployment Guide

## Quick Deploy to Netlify

### Option 1: Drag & Drop (Easiest)
1. Go to https://app.netlify.com
2. Log in to your account
3. Drag the entire `steppein-website` folder onto the Netlify dashboard
4. Your site will be live in seconds!

### Option 2: Netlify CLI
```bash
cd /Users/mmestey/Developer/SteppeinApp-fresh/steppein-website
netlify deploy --prod --dir=.
```
Then follow the prompts to create a new site.

### Option 3: Connect to GitHub
1. Push the `steppein-website` folder to a GitHub repo
2. Connect the repo in Netlify dashboard
3. Auto-deploys on every push

---

## Connect Your Domain (steppein.com)

### Step 1: Add Custom Domain in Netlify
1. Go to your site in Netlify dashboard
2. Click "Domain management" → "Add custom domain"
3. Enter: `steppein.com`
4. Netlify will provide DNS records

### Step 2: Update GoDaddy DNS
In your GoDaddy DNS settings, add these records:

**Option A: Point to Netlify DNS (Recommended)**
- Change nameservers to Netlify's nameservers
- Netlify will provide these in the dashboard

**Option B: Add CNAME/A Records**
| Type | Host | Value |
|------|------|-------|
| A | @ | 75.2.60.5 |
| CNAME | www | your-site-name.netlify.app |

### Step 3: Enable HTTPS
- Netlify automatically provides free SSL
- Click "Verify DNS" in Netlify once DNS propagates (5-30 min)
- Click "Provision certificate"

---

## Website Features

- **Boot brandmark** as favicon (mini logo)
- **GSAP scroll animations** (Acorns-style smooth effects)
- **New app mockups** showcasing the SteppeIn app
- **Full Steppein logo** in footer
- **Payment options section** for workers without bank accounts
- **Mobile responsive** design
- **Performance optimized** with caching headers

---

## Files Included

```
steppein-website/
├── index.html          # Main website
├── netlify.toml        # Netlify configuration
├── DEPLOY.md           # This file
└── images/
    ├── favicon-boot.png        # Boot brandmark (favicon)
    ├── steppein-logo-full.png  # Full logo with worker
    ├── steppein-logo.png       # Logo
    ├── app-browse-jobs.png     # App screenshot
    ├── app-job-details.png     # App screenshot
    └── app-worker-profile.png  # App screenshot
```

---

## Need Help?

Contact support@steppein.com or refer to:
- Netlify Docs: https://docs.netlify.com
- GoDaddy DNS: https://www.godaddy.com/help/change-nameservers-664
