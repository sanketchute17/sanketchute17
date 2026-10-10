# 🚀 GitHub Profile Upload Guide for @sanketchute17

This guide outlines how to upload your new premium GitHub Profile README and SVG assets to your GitHub special profile repository.

---

## 📌 Step 1: Create your GitHub Profile Repository

1. Go to [GitHub New Repository](https://github.com/new).
2. Set the **Repository Name** to exactly: `sanketchute17`
   > 💡 *GitHub will show a banner saying: "You found a secret! sanketchute17/sanketchute17 is a ✨special✨ repository that you can use to add a README.md to your GitHub profile."*
3. Make sure the repository visibility is **Public**.
4. Check **Add a README file** (optional, you will replace it with the new `README.md`).
5. Click **Create repository**.

---

## 📌 Step 2: Copy Package Files

Copy all files and folders from `sanketchute17-profile/` into your local `sanketchute17` repository directory:

```
sanketchute17/
├── README.md
├── UPLOAD-GUIDE.md
├── ASSET-NOTES.md
├── preview.html
└── assets/
    ├── hero.svg
    ├── about-life.svg
    ├── stack.svg
    ├── id-dashboard.svg
    ├── connect.svg
    ├── avatar.svg
    └── pointing-avatar.svg
```

---

## 📌 Step 3: Git Commit & Push Commands

Open your terminal or PowerShell inside the `sanketchute17` directory and run:

```bash
# Initialize git repository (if not already initialized)
git init

# Add all profile files and assets
git add .

# Commit changes
git commit -m "feat: Add premium animated SVG GitHub profile README"

# Ensure main branch name
git branch -M main

# Add your GitHub remote URL
git remote add origin https://github.com/sanketchute17/sanketchute17.git

# Push changes to GitHub
git push -u origin main
```

---

## 📌 Step 4: Verify Your Profile

1. Visit your GitHub profile page: [`https://github.com/sanketchute17`](https://github.com/sanketchute17).
2. Verify that all 5 SVG sections render cleanly:
   - **Hero Greeting** (`hero.svg`)
   - **Engineering Capabilities** (`about-life.svg`)
   - **Technology Stack** (`stack.svg`)
   - **Developer ID Dossier** (`id-dashboard.svg`)
   - **Connect & Socials** (`connect.svg`)
3. Click social badges and repository links below the images to test navigation.

---

## 💡 Cache Invalidation Tip

GitHub uses an image proxy (`camo.githubusercontent.com`) to cache images. If you edit an SVG file in the future and GitHub shows the cached old version:

1. Update the version parameter in `README.md`:
   ```markdown
   ![Introduction](./assets/hero.svg?v=2)
   ```
2. Commit and push the updated `README.md`. GitHub will immediately fetch the latest version.
