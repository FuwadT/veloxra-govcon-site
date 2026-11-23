# Veloxra, LLC — Public Website & AI Agent Interface (GitHub Pages)

This repository hosts the public-facing website for **Veloxra, LLC** and provides machine-readable endpoints (`/llms.txt`, `/agent-manifest.json`, Schema.org JSON-LD) so external and internal AI agents (Claude Code, Codex, AGY) can inspect and update the site in real time.

## Repository Structure
- `index.html` — Public-facing responsive GovCon website with embedded Schema.org JSON-LD.
- `styles.css` — Clean federal-grade stylesheet (mobile-responsive, high-contrast WCAG AA).
- `llms.txt` — Machine-readable plain-text/Markdown summary for AI agents.
- `agent-manifest.json` — Structured JSON manifest of entity identifiers, NAICS codes, capabilities, and team clearances.
- `docs/Veloxra_Capability_Statement.md` — Downloadable Federal Capability Statement.
- `robots.txt` & `sitemap.xml` — Search engine and AI crawler configuration.
- `.github/workflows/deploy-pages.yml` — Automatic GitHub Pages deployment on every push to `main`.

---

## How to Launch on GitHub Pages in 5 Minutes
1. **Create a GitHub Organization or Repo:** Create a repository (e.g., `veloxra-gov/veloxra-website`) and upload all files in this folder to the `main` branch.
2. **Enable GitHub Pages:** Go to **Settings -> Pages -> Build and deployment -> Source** and select **GitHub Actions**.
3. **Add All 4 Founders as Collaborators:** Go to **Settings -> Collaborators and teams** and invite Fuwad Tufail, Nhan Ngyugen, Ehson Ahmsa, and Husam Tufail with **Write** (or **Admin**) permissions so everyone can push updates in real time.
4. **Connect Custom Domain (`veloxra.com`):** In **Settings -> Pages -> Custom domain**, enter `veloxra.com`, enable **Enforce HTTPS**, and point your DNS `A` / `CNAME` records to GitHub Pages.

---

## Real-Time Multi-Person & AI Agent Editing Workflows
### 1. Instant Browser Editing (No Local Setup Needed)
- Any of the 4 founders can open the repo on `github.com`, press the **`.` (period)** key on their keyboard to launch **github.dev** (web VS Code), edit `index.html`, `llms.txt`, or `agent-manifest.json`, and commit directly to `main`. GitHub Actions redeploys the live site in ~30 seconds.

### 2. Local AI Agent Editing (Claude Code / Codex / AGY)
- Each founder clones the repo locally (`git pull` before editing) and instructs their AI agent:
  ```bash
  claude "Update the UEI and CAGE code across index.html, llms.txt, agent-manifest.json, and docs/Veloxra_Capability_Statement.md, then commit and push to main."
  ```
- **OPSEC Guardrail:** Never commit private EINs, bank account numbers, SSNs, or CUI into this public repository.
