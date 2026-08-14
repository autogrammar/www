# 🌐 AutoGrammar Ecosystem — Landing Page & Projects Hub (`www`)

Official landing page and interactive projects dashboard for the **AutoGrammar** ecosystem.

![AutoGrammar Projects Hub](assets/hero_banner.jpg)

## 🌟 Key Features

- **24-Hour Daily Cache Engine**: Auto-synchronizes repository stats, README files, tasks, and tags from GitHub REST API.
- **Project Purpose & Tasks**: Highlights the primary objective of all 25 repositories in the ecosystem.
- **Interactive Dependency Diagram**: Fullscreen Cytoscape.js directed network graph showing upstream dependencies and downstream dependants.
- **Categorized Use Case Tags**: Multi-tag filtering by `#nlp`, `#compiler`, `#dsl`, `#toon`, `#bnf`, `#fuzzing`, `#iterative`, `#grammar-check`, `#flashcards`, `#auth`, etc.
- **Triple View System**:
  1. `Grid View`: Rich glassmorphism project cards with task summaries and GitHub metrics.
  2. `Graph View`: Dynamic Cytoscape.js graph canvas with path highlighting.
  3. `Matrix View`: Complete tabular representation of ecosystem dependencies.

---

## 🛠️ Repository Structure

```
www/
├── index.html                  # Main application landing page
├── styles.css                  # Deep Space Glassmorphism design system
├── app.js                      # Application logic, Cytoscape graph & 24h cache manager
├── projects_cache.json         # Bundled daily GitHub API offline cache dataset
├── package.json                # Node.js project manifest
├── favicon.ico                 # Site favicon
├── assets/                     # Graphic assets and hero banner
│   └── hero_banner.jpg
├── vendor/                     # Standalone JS vendor libraries (Cytoscape, Marked)
│   ├── cytoscape.min.js
│   └── marked.min.js
├── scripts/                    # Automation scripts
│   └── update_github_cache.py  # Python daily cache update script
└── .github/
    └── workflows/              # GitHub Actions workflows
        ├── deploy.yml          # GitHub Pages automated deployment
        └── daily_cache_update.yml # Daily automated GitHub API sync cron job
```

---

## 🚀 Running Locally

```bash
# Clone the repository
git clone git@github.com:autogrammar/www.git
cd www

# Option 1: Run local dev server via Python
python3 -m http.server 8090

# Option 2: Run via NPM
npm run dev
```

Open `http://localhost:8090` in your web browser.

---

## 🔄 Daily Cache Update Command

To trigger an instant update of `projects_cache.json` with live GitHub REST API statistics and local workspace changes:

```bash
python3 scripts/update_github_cache.py
```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for details.
