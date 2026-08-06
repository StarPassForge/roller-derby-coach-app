# 🤝 Contributing to Roller Derby Coach App

First off — thank you! Whether you're a coach, skater, official, developer, or just someone who loves the sport, your contributions make this project better for the entire roller derby community across WFTDA, USARS, and JRDA leagues.

This guide explains how to get involved, what kinds of contributions we welcome, and how to submit your work.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Drill Submissions](#drill-submissions)
- [Rules Corrections](#rules-corrections)
- [Reporting Bugs](#reporting-bugs)
- [Requesting Features](#requesting-features)
- [JRDA-Specific Contributions](#jrda-specific-contributions)
- [Style Guidelines](#style-guidelines)
- [License](#license)

---

## 📜 Code of Conduct

This project follows a simple rule: **be excellent to each other.** We are a community of people who love roller derby. Harassment, discrimination, or hostility of any kind will not be tolerated.

This applies to all project spaces — GitHub issues, pull requests, discussions, and any affiliated channels.

---

## 🏋️ Ways to Contribute

You don’t need to be a developer to contribute meaningfully:

| Contribution Type | Who It’s For |
|---|---|
| Bug reports | Anyone who finds something broken |
| Feature requests | Coaches, managers, skaters with ideas |
| Drill submissions | Coaches and trainers |
| Rules content | Officials and rules committee members |
| Code contributions | Developers |
| Documentation improvements | Writers, coaches, anyone |
| JRDA-specific feedback | Junior league coaches and guardians |
| Translation / localization | Bilingual community members |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [Git](https://git-scm.com/)
- A GitHub account

### Local Setup

```bash
# 1. Fork the repository on GitHub, then clone your fork
git clone https://github.com/YOUR_USERNAME/roller-derby-coach-app.git
cd roller-derby-coach-app

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev

# 4. Create a branch for your changes
git checkout -b feature/your-feature-name
```

> Use descriptive branch names like `feature/jrda-age-divisions`, `fix/roster-export-bug`, or `docs/setup-guide`.

---

## 🔀 Submitting a Pull Request

1. **Make your changes** on your feature branch
2. **Test your work** — make sure nothing is broken (`npm test`)
3. **Write a clear commit message** — e.g. `Add JRDA age eligibility flag to roster module`
4. **Push your branch** to your fork: `git push origin feature/your-feature-name`
5. **Open a Pull Request** against the `main` branch of this repository
6. **Fill out the PR template** — describe what you changed and why
7. A maintainer will review your PR, leave feedback if needed, and merge when ready

### PR Checklist

- [ ] My changes are scoped to a single feature or fix
- [ ] I have tested my changes locally
- [ ] I have updated relevant documentation if needed
- [ ] My code follows the project’s style guidelines
- [ ] I have not introduced any new dependencies without discussion

---

## 🏋️ Drill Submissions

Drill contributions are one of the most valuable things the community can offer. To submit a drill:

1. Navigate to the `drills/` folder
2. Copy the drill template: `drills/TEMPLATE.md`
3. Fill in all required fields:
   - **Name** — short, memorable drill name
   - **Ruleset** — WFTDA, USARS, JRDA, or All
   - **Focus Area** — e.g. blocking, jamming, footwork, pack awareness
   - **Skill Level** — Beginner / Intermediate / Advanced
   - **Duration** — estimated minutes
   - **Description** — clear step-by-step instructions
   - **Coaching Tips** — what to watch for, common mistakes
   - **Variations** — optional progressions or modifications
4. Save as `drills/your-drill-name.md` and open a Pull Request

> Drills tagged for **JRDA** should note any age-appropriate modifications and keep safety considerations front and center.

---

## 📖 Rules Corrections

Rulebooks change. If you spot an outdated or incorrect rules entry:

1. Open a GitHub Issue with the label `rules-correction`
2. Include:
   - The governing body (WFTDA, USARS, or JRDA)
   - The specific rule or section
   - A direct link or citation to the current official rulebook
   - What the app currently says vs. what it should say
3. Or submit a PR directly to `rules/` with your correction and citation

---

## 🐛 Reporting Bugs

Found something broken? Please [open a GitHub Issue](../../issues/new) and include:

- A clear title describing the problem
- Steps to reproduce the bug
- What you expected to happen
- What actually happened
- Your browser / device / OS (if relevant)
- Screenshots if helpful

---

## 💡 Requesting Features

Have an idea? [Open a GitHub Issue](../../issues/new) with the label `feature-request` and tell us:

- What problem does this solve for coaches or leagues?
- Which ruleset(s) does it apply to (WFTDA, USARS, JRDA, or all)?
- Any examples from other tools you’ve seen do it well?

Feature requests from active coaches and officials are especially valued — you know what the bench actually needs.

---

## 💚 JRDA-Specific Contributions

Junior roller derby has unique needs — age divisions, guardian consent workflows, developmentally appropriate drills, and rulebook differences. We actively want input from:

- JRDA coaches and team managers
- Junior league officials
- Parents and guardians involved in league administration
- JRDA skaters (yes, your perspective matters!)

When submitting JRDA-specific issues or PRs, use the label `jrda` so maintainers can prioritize appropriately. If you’re unsure whether something is JRDA-specific or general, just ask in the issue.

---

## 🎨 Style Guidelines

### Code
- Follow the existing code style (enforced by the project linter)
- Run `npm run lint` before submitting
- Prefer clarity over cleverness — this codebase is read by people who coach roller derby, not just engineers

### Documentation & Markdown
- Use plain, clear language — write for coaches, not just developers
- Use headers, bullet points, and tables to aid scannability
- Emoji in headings is welcome and on-brand 🛼

### Commit Messages
- Use the imperative mood: `Add`, `Fix`, `Update`, `Remove`
- Keep the first line under 72 characters
- Reference issue numbers where relevant: `Fix roster export crash (#42)`

---

## 📄 License

By contributing to this project, you agree that your contributions will be licensed under the **GNU General Public License v3.0**, the same license that covers this project. This keeps everything open for the whole community.

See the [LICENSE](../LICENSE) file for details.

---

*Built with love for the roller derby community — WFTDA, USARS, and JRDA — by the StarPassForge collective.*
*Hit hard. Coach smart. Share freely.*
