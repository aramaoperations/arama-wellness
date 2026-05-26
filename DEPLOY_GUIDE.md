# ārāma Wellness OS — GitHub Pages Deployment Guide

**Target URL:** `https://aramaoperations.github.io/arama-wellness/`

---

## Files to Deploy

| File | Purpose | URL after deploy |
|---|---|---|
| `ARAMA_OS_V7.html` | Staff / Operations portal | `.../ARAMA_OS_V7.html` |
| `customer.html` | Customer-facing portal | `.../customer.html` |
| `staff-register.html` | Public staff registration | `.../staff-register.html` |
| `arama-qr.html` | QR code generator | `.../arama-qr.html` |
| `manifest.json` | PWA manifest | `.../manifest.json` |

---

## Option A — GitHub Desktop (Easiest, no terminal needed)

### Step 1 — Install GitHub Desktop
Download from https://desktop.github.com and sign in with the `aramaoperations` GitHub account.

### Step 2 — Clone the repository
1. Click **File → Clone repository**
2. Search for `aramaoperations/arama-wellness`
3. Choose a local folder (e.g. `C:\Users\AARYAN\Documents\GitHub\arama-wellness`)
4. Click **Clone**

### Step 3 — Copy your files in
Open the cloned folder in Windows Explorer and copy these files into it:
- `ARAMA_OS_V7.html`
- `customer.html`
- `staff-register.html`
- `arama-qr.html`
- `manifest.json`

### Step 4 — Commit and push
1. GitHub Desktop will show all 5 files as changes
2. In the **Summary** box type: `Deploy ārāma Wellness OS v7`
3. Click **Commit to main**
4. Click **Push origin** (top bar)

### Step 5 — Enable GitHub Pages
1. Go to `https://github.com/aramaoperations/arama-wellness`
2. Click **Settings → Pages** (left sidebar)
3. Under **Source** select: **Deploy from a branch**
4. Branch: **main** / Folder: **/ (root)**
5. Click **Save**

GitHub will show a banner: *"Your site is live at https://aramaoperations.github.io/arama-wellness/"*
(Takes 1–3 minutes first time.)

---

## Option B — Git via Terminal (If git is installed)

Open PowerShell or Command Prompt and run:

```powershell
# 1. Clone repo (first time only)
git clone https://github.com/aramaoperations/arama-wellness.git
cd arama-wellness

# 2. Copy your files into this folder, then:
git add ARAMA_OS_V7.html customer.html staff-register.html arama-qr.html manifest.json

# 3. Commit and push
git commit -m "Deploy ārāma Wellness OS v7"
git push origin main
```

For future updates (after editing a file):
```powershell
cd arama-wellness
git add -A
git commit -m "Update: describe what changed"
git push origin main
```

---

## Option C — Upload directly on GitHub website (No software needed)

1. Go to `https://github.com/aramaoperations/arama-wellness`
2. Click **Add file → Upload files**
3. Drag and drop all 5 files onto the upload area
4. Scroll down, type a commit message: `Deploy ārāma Wellness OS v7`
5. Click **Commit changes**

Then enable Pages as in Step 5 above.

---

## After Deployment — Verify

Open these URLs in your browser to confirm everything is live:

- ✅ `https://aramaoperations.github.io/arama-wellness/ARAMA_OS_V7.html`
- ✅ `https://aramaoperations.github.io/arama-wellness/customer.html`
- ✅ `https://aramaoperations.github.io/arama-wellness/staff-register.html`
- ✅ `https://aramaoperations.github.io/arama-wellness/arama-qr.html`

---

## QR Codes — After Going Live

Once `customer.html` is live, open `arama-qr.html` and:
1. Upload your ārāma logo PNG
2. The default URL is already set to the live customer portal
3. Generate and download QR cards for all 33 locations

---

## Future Updates

Whenever you edit any HTML file in your `arama wellness os` folder:
1. Copy the updated file into your cloned `arama-wellness` folder
2. Commit and push (GitHub Desktop or terminal)
3. Site updates live within ~30 seconds

---

## Important Notes

- **localStorage is per-browser, per-device** — data entered in the ops portal on a laptop is not visible on a different laptop. For a shared data store, you would need a backend (not in scope for v7).
- **GitHub Pages is public** — anyone with the URL can access the pages. The ops portal is protected by login (username/password), but the URLs themselves are not hidden.
- **HTTPS is automatic** — GitHub Pages serves all content over HTTPS, which is required for the PWA install prompt.
- **Support / maintenance:** tech@arama.asia

---

*ārāma Wellness OS v7 — Deployed via GitHub Pages*
