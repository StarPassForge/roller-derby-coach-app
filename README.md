# 🛼 Roller Derby Coach App

> A free, open-source coaching toolkit for roller derby teams — built to streamline drill planning,
> roster management, rules reference, and performance analytics from the track to the whiteboard.
> Supports WFTDA, USARS, and JRDA leagues at all levels of play.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Repo: StarPassForge](https://img.shields.io/badge/org-StarPassForge-blueviolet)](https://github.com/StarPassForge)

---

## 📖 Overview

The **Roller Derby Coach App** is a modular coaching assistant designed for head coaches, assistant
coaches, and team managers at all levels of roller derby competition — from junior leagues to elite
bout teams. It centralizes the tools a coaching staff actually uses — drill libraries, live roster
tracking, rules quick-reference, and post-bout analytics — into a single, open platform that any
WFTDA, USARS, or JRDA league can self-host, fork, and adapt.

The project is maintained under the **StarPassForge** organization and is proudly licensed under the
[GNU General Public License v3.0](LICENSE), meaning every improvement stays open for the community.

---

## 🗂️ Repository Structure

```
roller-derby-coach-app/
├── drills/          # Drill library and practice plan builder
├── rules/           # WFTDA/USARS/JRDA rules reference and quick-lookup tools
├── roster/          # Skater profiles, eligibility tracking, and lineup management
├── analytics/       # Bout statistics, performance metrics, and reporting
├── ui/              # Front-end components, layouts, and theming
└── docs/            # Project documentation, setup guides, and API references
```

### Folder Details

| Folder | Purpose |
|---|---|
| `drills/` | A searchable library of roller derby drills tagged by skill level, focus area (blocking, jamming, footwork, etc.), and session duration. Supports filtering by ruleset (WFTDA, USARS, JRDA) so coaches can surface age- and rules-appropriate content. Includes a practice plan builder to sequence drills into full session templates. |
| `rules/` | A structured, searchable digest of current WFTDA, USARS, and JRDA rulebooks. Designed for quick on-bench lookups — covers penalties, gameplay definitions, officiating signals, and rules-change changelogs across all three governing bodies. |
| `roster/` | Skater profile management including insurance status, minimum skills certification, dues standing, and game-day eligibility flags. Supports multi-team leagues, travel squad exports, and JRDA age-eligibility tracking. |
| `analytics/` | Bout-level and season-level statistics for skaters and units. Tracks jam points, lead jammer %, blocker efficiency, penalty heat maps, and trend lines across a season. Compatible with WFTDA, USARS, and JRDA scoring formats. |
| `ui/` | Shared front-end components (navigation, cards, modals, data tables) and global theming. Built to be responsive for both desktop coaching boards and mobile sideline use. |
| `docs/` | Setup and installation guides, architecture decisions, API reference, and contributor documentation. Start here if you're deploying or contributing. |

---

## ✨ Features

- **Drill Library** — Browse, filter, and build practice sessions from a growing community drill bank; filter by WFTDA, USARS, or JRDA ruleset
- **Rules Quick-Reference** — Search penalties and definitions across WFTDA, USARS, and JRDA rulebooks without leaving the bench
- **Roster Management** — Track skater eligibility, certifications, and game-day availability; includes JRDA age-eligibility flags
- **Performance Analytics** — Visualize individual and unit stats across bouts and seasons for all rulesets
- **Session Planning** — Assemble full practice plans with time estimates and skill focus tags
- **Responsive UI** — Works on coaching laptops, tablets, and phones at the track

---

## 🗺️ Feature Roadmap

### Near-Term (v0.x)
- [ ] Drill submission flow for community contributions with coach review queue
- [ ] CSV import/export for roster data (league management system compatibility)
- [ ] Penalty tracker for live bout use (WFTDA, USARS, and JRDA penalty sets)
- [ ] Dark mode and high-contrast theming for low-light venues

### Mid-Term (v1.x)
- [ ] Role-based access control (head coach, assistant coach, manager, skater view)
- [ ] Practice attendance and participation logging
- [ ] Drill video embed support (self-hosted or linked)
- [ ] Multi-language support (rulebook localization)
- [ ] JRDA-specific age division management and guardian consent tracking
- [ ] Mobile app wrapper (PWA or React Native)

### Long-Term (v2.x+)
- [ ] AI-assisted practice plan suggestions based on team weaknesses
- [ ] Season scheduling and opponent scouting notes
- [ ] Integration with league management platforms (WFTDA, USARS, and JRDA member portals)
- [ ] Live game dashboard with real-time stat entry
- [ ] **JamStats integration** *(see below)*

---

## 🔗 Future Integration: JamStats

A planned integration with **[JamStats](https://github.com/dhmay/jamstats)** will allow the app to automatically
import official bout statistics directly into the analytics module, eliminating manual data entry
after games.

**Planned integration scope:**

- **Bout data import** — Pull jam-by-jam scoring, lead jammer results, and penalty logs from
  JamStats exports into the `analytics/` module
- **Skater stat sync** — Map JamStats skater records to existing `roster/` profiles by name or
  skater number
- **Historical trend analysis** — Aggregate multiple JamStats imports into season-long performance
  curves and comparative reports
- **Ruleset tagging** — Tag imported bouts by governing body (WFTDA, USARS, JRDA) for
  accurate cross-ruleset analytics
- **Export compatibility** — Produce JamStats-compatible output from manually entered bout data
  for leagues that track both systems

> **Status:** In design — API shape and auth model under discussion. Contributions and feedback
> from JamStats users are welcome. See [`docs/integrations/jamstats.md`](docs/) for the current
> integration spec draft.

---

## 🚀 Getting Started

See [`docs/SETUP.md`](docs/) for full installation and configuration instructions.

```bash
# Clone the repo
git clone https://github.com/StarPassForge/roller-derby-coach-app.git
cd roller-derby-coach-app

# Install dependencies
npm install        # or yarn install

# Start the development server
npm run dev
```

---

## 🤝 Contributing

Contributions are welcome from coaches, developers, officials, and skaters alike — across WFTDA,
USARS, and JRDA communities. Please read [`docs/CONTRIBUTING.md`](docs/) before opening a pull
request.

- **Bug reports & feature requests:** Open a GitHub Issue
- **Drill submissions:** Use the drill submission form in the app (or PR directly to `drills/`)
- **Rules corrections:** Open a PR with a link to the applicable WFTDA, USARS, or JRDA rules citation
- **JRDA-specific feedback:** Junior league coaches and officials are especially encouraged to weigh in on age-division features

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0**.

You are free to use, modify, and distribute this software under the terms of the GPL-3.0. Any
derivative works must also be distributed under the same license, keeping the project open for
the entire roller derby community.

See the [`LICENSE`](LICENSE) file for the full license text, or visit
[gnu.org/licenses/gpl-3.0](https://www.gnu.org/licenses/gpl-3.0).

---

## 🏁 Acknowledgments

Built with love for the roller derby community — WFTDA, USARS, and JRDA — by the **StarPassForge** collective.
*Hit hard. Coach smart. Share freely.*
