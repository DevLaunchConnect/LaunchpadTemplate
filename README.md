# Launchpad Template 🚀

[![CI Status](https://github.com/DevLaunchConnect/launchpad-template/actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml)  
![Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen)

Reusable starter repo for **every** Launchpad student squad—pre‑loaded with ESLint, Prettier, unit tests, and a GitHub Actions CI pipeline. Works with **Node / React, Python / Django / Flask, Go, Rust, or any CLI project**. The goal is *zero boilerplate debates* so squads can focus on shipping features.

---

# Quick Start (3 Steps)

 1. **Clone the template**
 
    ```bash
    # Click “Use this template” in GitHub → create <YOUR‑REPO>, then:
    git clone git@github.com:DevLaunchConnect/<YOUR‑REPO>.git
    cd <YOUR‑REPO>
 2. **Install dependencies**
 
    ```bash
    ## Node example
       npm install
    # Python example
      python -m venv venv
      source venv/bin/activate
      pip install -r requirements.txt
  3. **Run tests or start the dev server**
 
     ```bash
     ## Unit tests
        npm test           # or: pytest
       # Local dev server
        npm run dev        # or: python manage.py runserver


# Scripts
| Command                    | Purpose                              |
| -------------------------- | ------------------------------------ |
| `npm run dev` / `make dev` | Start local development server       |
| `npm run lint` / `flake8`  | Lint the entire code‑base            |
| `npm run format` / `black` | Auto‑format files to style guide     |
| `npm test` / `pytest`      | Run unit tests and generate coverage |

CI Gate: a pull request fails if <br> 
<br>
• tests fail, <br>
• global coverage drops below 70 %, or <br>
• code fails lint / format checks.<br>


# Folder Structure (starter)
  
    <YOUR‑REPO>
    ├── src/ or app/                    # main application code
    │   ├── index.js / app.py / main.go # entrypoint (replace as needed)
    │   └── modules/                    # feature modules / packages
    ├── test/                           # unit tests
    ├── .github/workflows/ci.yml        # GitHub Actions pipeline
    ├── .eslintrc / pyproject.toml      # lint config (per language)
    └── README.md

Swap or extend folders to match your language or framework.

<br>

# Branch & PR Policy

Create a feature branch off main. <br>
<br>
Open a pull request; require one squadmate review plus green CI.<br>
<br>
Squash & merge when approved, then delete the branch.<br>

<br>

# Customization Checklist ✅

- [ ] Update the CI & Coverage badges to point at your new repo path.  
- [ ] Swap ESLint / flake8 / golangci‑lint rules to match your language.  
- [ ] Replace the “Hello Launchpad 👋” starter file with your actual entrypoint.  
- [ ] Edit `.github/workflows/ci.yml` to run your build & test commands.

<br>

# License


Released under the MIT license — share freely, learn loudly.


