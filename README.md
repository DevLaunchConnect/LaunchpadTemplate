# Launchpad Template 🚀

[![Live Preview](https://img.shields.io/badge/preview-live‑green?logo=vercel)](https://example.com)  
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

## Scripts
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


## Folder Structure (starter)
  
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

## Secrets & Environment Variables

1. Fill real keys in `.env` locally.  
2. **Never commit `.env`** – it’s ignored by .gitignore.  
3. For CI / GitHub Actions add secrets in **Repo → Settings → Secrets & variables → Actions**  
   (e.g., `STRIPE_TEST_KEY`, `DATABASE_URL`).  
4. If you need the secret in Vercel/Render, replicate the same key there.
<br>

## Branch & PR Policy

Create a feature branch off main. <br>
<br>
Open a pull request; require one squadmate review plus green CI.<br>
<br>
Squash & merge when approved, then delete the branch.<br>

<br>

## Contributing 🙋

Student squads should follow these steps for every change:

1. **Branch** off `main` using a descriptive name (e.g., `feature/login-form`).
2. **Write / update tests** so coverage stays ≥ 70 %.
3. **Run lint & format** locally (`npm run lint && npm run format` or `flake8 && black .`).
4. Open a **PR** — one teammate must **Approve** and **CI must be green**.
5. Choose **Squash & merge** so `main` history stays one‑commit‑per‑PR.

 <br>

## Customization Checklist ✅

- [ ] Update the CI & Coverage badges to point at your new repo path.  
- [ ] Swap ESLint / flake8 / golangci‑lint rules to match your language.  
- [ ] Replace the “Hello Launchpad 👋” starter file with your actual entrypoint.  
- [ ] Edit `.github/workflows/ci.yml` to run your build & test commands.

<br>

# Dev Squad Usage Guide 🛠️🚦

## 0 · Guard‑rails at a Glance 
| Guard‑rail              | Why it exists                      | What you must do                                     |
| ----------------------- | ---------------------------------- | ---------------------------------------------------- |
| `.editorconfig`         | Enforces 2‑space indent, LF, UTF‑8 | Keep “Respect .editorconfig” on in your IDE          |
| `.gitignore` (polyglot) | Blocks caches & build artifacts    | Leave as‑is; add patterns if needed                  |
| **CI workflow**         | Runs `TEST_CMD` on every push/PR   | Set `TEST_CMD` variable (`npm test`, `pytest`, etc.) |
| Branch rule             | Forces review + green CI           | Work in feature branches; PR → review → merge        |
| Security defaults       | Dependabot, secret‑scanning        | Merge security PRs; never commit secrets             |

## 1 · Spin‑Up Checklist

- [ ] Clone repo locally.

- [ ] Install stack deps (npm install, pip install -r requirements.txt, etc.).

- [ ] Copy a lint config from lint-configs/ if desired.

- [ ] Write at least one unit test in test/.

- [ ] Commit & push initial scaffold.

## 2 · Tell CI how to test your stack
1. Settings → Secrets and variables → Actions → Variables → New.
<br>
2. Name: TEST_CMD Value: e.g., pytest, go test ./..., npm test.
<br>
3. Save — next CI run uses it.

## 3 · Local Dev Tips
| Task        | Command (examples)                      |
| ----------- | --------------------------------------- |
| Lint code   | `npm run lint` / `flake8`               |
| Auto‑format | `npm run format` / `black .`            |
| Run tests   | `npm test` / `pytest` / `go test ./...` |

## 4 · Security / Secrets
Store API keys in Settings → Secrets → Actions; access via process.env.MY_KEY or $MY_KEY.
Dependabot alerts appear as PRs—merge them promptly.


##  5 · Troubleshooting CI

| Symptom                         | Fix                                               |
| ------------------------------- | ------------------------------------------------- |
| `npm ERR! missing script: test` | Set `TEST_CMD` to a real command.                 |
| Coverage fails threshold        | Write more tests or adjust threshold in workflow. |
| “command not found”             | Install tools or use dockerized test command.     |

##  6 · Final Demo‑Ready Checklist

- [ ] main CI green.

- [ ] Coverage ≥ 70 % (or agreed target).

- [ ] Lint passes.

- [ ] README updated with run instructions.

- [ ] Staging deployment refreshed (if applicable).

## License


Released under the MIT license — share freely, learn loudly.

"" 
"" 
