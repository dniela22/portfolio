# Cybersecurity Portfolio

A clean, dark-themed personal portfolio site for cybersecurity professionals.
Deploys automatically to GitHub Pages.

## Live URL
Once deployed: `https://yourusername.github.io/portfolio`

---

## One-Time GitHub Pages Setup (do this first)

1. Push your code to GitHub (steps below)
2. In your GitHub repo, go to **Settings → Pages**
3. Under **Source**, select **GitHub Actions**
4. Save — that's it. The next push will trigger a deploy.

---

## Personalize It

### 1. Your Name & Info
Open `index.html` and find/replace:
- `Your Full Name` → your actual name
- `YN` (avatar initials) → your initials
- `you@email.com` → your email address
- `yourprofile` → your LinkedIn handle
- `yourusername` → your GitHub username

### 2. Add Your Headshot
1. Add your photo to `assets/headshot.jpg`
2. In `index.html`, find the `<div class="avatar-initials">YN</div>` line
3. Replace it with:
   ```html
   <img src="assets/headshot.jpg" alt="Your Name" class="headshot-img" />
   ```

### 3. Update Experience
Edit the `.exp-item` blocks in `index.html` with your actual dates, roles, and descriptions.

### 4. Add/Edit Projects
Duplicate a `.project-card` block and fill in your own project details.
Update the `href="#"` on `.proj-link` to point to your GitHub repos.

### 5. Update Skills
Edit the `.tag` items inside each `.skill-card` to match your actual skillset.

### 6. Resume
Drop your resume PDF at `assets/resume.pdf` so the download button works.

### 7. Nav Logo
Change `YourName.sec` in the `.nav-logo` div to your preferred display name.

---

## Deploy with Git Bash

### First-time setup
```bash
# Navigate to the portfolio folder (adjust path as needed)
cd /c/Users/YourName/Downloads/portfolio

# Initialize git
git init

# Connect to your GitHub repo (create the repo on github.com first — name it "portfolio")
git remote add origin https://github.com/YOURUSERNAME/portfolio.git

# Push everything
git add .
git commit -m "feat: launch portfolio"
git branch -M main
git push -u origin main
```

Then go to **github.com → your repo → Settings → Pages → Source: GitHub Actions** and save.

### After any change
```bash
git add .
git commit -m "update: describe your change here"
git push
```

GitHub will automatically run the workflow and publish your updated site.
Check progress under the **Actions** tab in your GitHub repo.

---

## File Structure
```
portfolio/
├── index.html                        ← Main page (edit this!)
├── css/
│   └── style.css                     ← All styles
├── assets/
│   ├── headshot.jpg                  ← Your photo (add this)
│   └── resume.pdf                    ← Your resume (add this)
├── .github/
│   └── workflows/
│       └── deploy.yml                ← Auto-deployment config (don't touch)
└── README.md                         ← This file
```
