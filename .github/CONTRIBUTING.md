# Contributing to AI SQL Assistant

Thank you for considering contributing to **AI SQL Assistant**! 🎉  
Every contribution — from a typo fix to a new feature — helps make this project better for everyone.

---

## Table of Contents

- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Improving Documentation](#improving-documentation)
  - [Submitting Code](#submitting-code)
- [Development Setup](#development-setup)
- [Code Style Guidelines](#code-style-guidelines)
- [Commit Message Convention](#commit-message-convention)
- [Pull Request Process](#pull-request-process)
- [Community Standards](#community-standards)

---

## Getting Started

1. **Fork** the repository on GitHub.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/AI_SQL_Assistant.git
   cd AI_SQL_Assistant
   ```
3. **Create a branch** for your work:
   ```bash
   git checkout -b feat/my-awesome-feature
   ```

---

## How to Contribute

### Reporting Bugs

If you find a bug, please [open an issue](https://github.com/invo-coder19/AI_SQL_Assistant/issues/new?template=bug_report.md) and include:

- A clear, descriptive title
- Steps to reproduce the problem
- Expected vs. actual behavior
- Your environment (OS, Python version, browser if relevant)
- Any relevant logs or screenshots

> **Note:** Never include your `OPENAI_API_KEY` or other credentials in a bug report.

### Suggesting Features

Got an idea? [Open a feature request](https://github.com/invo-coder19/AI_SQL_Assistant/issues/new?template=feature_request.md) and describe:

- The problem it solves or the use case it covers
- A proposed solution (even a rough sketch helps)
- Any alternatives you considered

### Improving Documentation

Documentation improvements are always welcome:

- Fix typos or broken links in `README.md`
- Improve code comments or docstrings in `app.py` / `services/sql_generator.py`
- Add examples to the README

### Submitting Code

We welcome bug fixes, performance improvements, and new features. Please check open issues first to avoid duplication.

---

## Development Setup

### Prerequisites

- Python **3.9+**
- `pip` / `venv`
- An OpenAI API key (optional — rule-based fallback works without one)

### Installation

```bash
# 1. Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS / Linux

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set up environment variables
copy .env.example .env       # Windows
# cp .env.example .env       # macOS / Linux
# Edit .env and add your OPENAI_API_KEY (optional)

# 4. Run the development server
python app.py
```

The app will be available at **http://localhost:5000**.

### Running the Smoke Tests

```bash
python _smoke_test.py
```

---

## Code Style Guidelines

### Python

- Follow [**PEP 8**](https://peps.python.org/pep-0008/).
- Use **4-space indentation** (no tabs).
- Keep line length ≤ **100 characters**.
- Add docstrings to all public functions and classes.
- Type hints are encouraged for new functions.

### JavaScript / HTML / CSS

- Use **2-space indentation**.
- Keep frontend logic in `static/script.js`; do not embed scripts in HTML.
- Keep styles in `static/style.css`.

### Project Structure

| Path | Purpose |
|---|---|
| `app.py` | Flask entry point & API routes |
| `services/sql_generator.py` | AI + rule-based SQL engine |
| `templates/index.html` | Jinja2 HTML template |
| `static/style.css` | Dark-theme CSS |
| `static/script.js` | Frontend logic |

---

## Commit Message Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short summary>
```

| Type | When to use |
|---|---|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation changes only |
| `style` | Code formatting (no logic change) |
| `refactor` | Code restructure without behaviour change |
| `test` | Adding or updating tests |
| `chore` | Build process, dependencies, config |

**Examples:**

```
feat(sql-engine): add support for JOIN queries
fix(api): handle empty query body with 400 response
docs(readme): update quick-start instructions
```

---

## Pull Request Process

1. **Ensure your branch is up to date** with `main`:
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```
2. **Run smoke tests** and make sure everything passes.
3. **Open a PR** against the `main` branch using the pull request template.
4. **Fill in the PR template** — describe what you changed, why, and how to test it.
5. **Link related issues** using `Closes #<issue-number>` in the PR description.
6. **Wait for review** — the maintainer will review and may request changes.
7. Once approved, your PR will be **squash-merged**.

> Small, focused PRs are much easier to review and are merged faster. Avoid bundling unrelated changes.

---

## Community Standards

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).  
Be kind, respectful, and constructive. We are all here to learn and build together. 🙌
