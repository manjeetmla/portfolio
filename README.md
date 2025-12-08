# Portfolio Website (Manjeet Kumar)

This repository contains a modern, responsive single-page portfolio built with Tailwind CSS and plain JavaScript.

Files:
- `index.html` — Tailwind-based main page (hero, skills, experience, projects, contact)
- `styles.css` — (kept for legacy styles; most layout uses Tailwind utility classes)
- `script.js` — small UI interactions (nav, smooth scroll) — some logic is inline in `index.html` for the typewriter
- `resume/manjeet_kumar_resume_one.pdf` — linked resume (already in your `resume/` folder)

Preview locally (from this repository root):

Using Python 3 (simple HTTP server):

```bash
# from /Users/manjeet/Desktop/Portfolio
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

Notes & next steps:
- The site uses the Tailwind CDN for styling and Font Awesome CDN for icons — no build step required to preview.
- I updated `index.html` to the provided Tailwind template and linked the Download Resume button to `./resume/manjeet_kumar_resume_one.pdf`.
- If you'd like, I can:
	- Extract exact text from your resume and populate the About and Experience sections.
	- Replace placeholder project links with live/demo/GitHub URLs.
	- Add a profile photo from `photos/` and update image alt text.
	- Prepare a deploy config for GitHub Pages, Netlify, or Vercel.

Tell me which of the next steps you want me to do and I’ll proceed.

Deployment to GitHub Pages (automatic)

I added a GitHub Actions workflow at `.github/workflows/deploy-pages.yml` that will publish the repository root to GitHub Pages whenever you push to the `main` branch. No build step is required — the workflow uploads the repo contents and deploys them.

How to publish this repo to GitHub (quick steps)

1. Create a new repository on GitHub (for example `manjeet-portfolio`).
2. From your local workspace run:

```bash
# from /Users/manjeet/Desktop/Portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin git@github.com:<your-username>/<your-repo>.git
git push -u origin main
```

3. After you push, GitHub Actions will run the `deploy-pages.yml` workflow and publish the site. You can check the Actions tab in your repository for status.

4. The site will be available at `https://<your-username>.github.io/<your-repo>/` (or at the Pages URL shown on the repository Settings > Pages page).

Notes & alternatives
- If you prefer a different workflow (e.g., use `gh-pages` branch or a build step with Node), tell me and I can create that.
- If your repo already exists and uses a different default branch, update the workflow `push.branches` to match.
