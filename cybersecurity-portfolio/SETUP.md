# How to publish this portfolio (10 minutes)

You have two things here:
1. **`profile-README.md`** — your GitHub *profile* landing page.
2. **`portfolio/`** — your portfolio *repository*.

---

## Part 1 — Profile README (the page people see on your GitHub profile)

GitHub shows a special README at the top of your profile if you create a repo **named exactly the same as your username**.

1. Create a new repository named **exactly your username** (e.g. if you're `AhmetUmutBulut`, name the repo `AhmetUmutBulut`). Make it **Public** and tick "Add a README".
2. Replace that README's contents with the contents of **`profile-README.md`**.
3. Find-and-replace every `[your-username]`, `[your-profile]`, and `[your.email@example.com]` with your real details.
4. Commit. It now shows on your profile page.

---

## Part 2 — Portfolio repository

### Option A — via the GitHub website (no command line)
1. Create a new **Public** repo called **`cybersecurity-portfolio`**.
2. Upload the contents of the **`portfolio/`** folder (the `README.md`, the `projects/` folder, and `assets/`).
3. Add your screenshots into `assets/` and update the `> Screenshots:` lines in each project file to point to them.

### Option B — via command line
```bash
cd portfolio
git init
git add .
git commit -m "Add cybersecurity portfolio"
git branch -M main
git remote add origin https://github.com/[your-username]/cybersecurity-portfolio.git
git push -u origin main
```

---

## Before you share the link — checklist
- [ ] Replaced all `[your-username]` / `[your-profile]` / `[your.email@example.com]` placeholders
- [ ] Added real screenshots to `assets/` and linked them in each project
- [ ] Added the pentest report PDF to `assets/` (redact sensitive host detail first)
- [ ] Confirmed nothing points to a real, non-consenting target
- [ ] Updated your CV's portfolio link to `github.com/[your-username]/cybersecurity-portfolio`
- [ ] Pinned the `cybersecurity-portfolio` repo on your profile (Customize your pins)

## Tip
Adding screenshots is what turns "he says he did it" into "he clearly did it." Do that before you send the link anywhere.
