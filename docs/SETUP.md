# 🚀 Setup Guide — Roller Derby Coach App

This guide walks you through installing, configuring, and running the Roller Derby Coach App locally. It also covers environment variables, common troubleshooting steps, and deployment basics.

---

## 📋 Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Running Locally](#running-locally)
- [Running Tests](#running-tests)
- [Project Structure Overview](#project-structure-overview)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [Getting Help](#getting-help)

---

## ✅ Prerequisites

Before you begin, make sure you have the following installed:

| Tool | Minimum Version | Notes |
|---|---|---|
| [Node.js](https://nodejs.org/) | v18.0.0 | LTS version recommended |
| [npm](https://www.npmjs.com/) | v9.0.0 | Comes with Node.js |
| [Git](https://git-scm.com/) | Any recent version | For cloning the repo |

> **Optional:** [Yarn](https://yarnpkg.com/) can be used in place of npm for all commands below.

---

## 📦 Installation

### 1. Fork and Clone the Repository

If you plan to contribute, fork the repo first on GitHub, then clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/roller-derby-coach-app.git
cd roller-derby-coach-app
```

If you just want to run it locally without contributing:

```bash
git clone https://github.com/StarPassForge/roller-derby-coach-app.git
cd roller-derby-coach-app
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

This will install all packages listed in `package.json`, including dev dependencies.

---

## 🔐 Environment Variables

Copy the example environment file and fill in your values:

```bash
cp .env.example .env
```

Then open `.env` in your editor. Key variables:

| Variable | Description | Required |
|---|---|---|
| `APP_PORT` | Port the dev server runs on (default: `3000`) | No |
| `DATABASE_URL` | Connection string for your local database | Yes |
| `SESSION_SECRET` | Secret key for session management | Yes |
| `JAMSTATS_API_URL` | Base URL for JamStats integration (when available) | No |
| `NODE_ENV` | Set to `development` for local work | Yes |

> **Never commit your `.env` file.** It is already listed in `.gitignore`.

---

## 🖥️ Running Locally

### Start the Development Server

```bash
npm run dev
# or
yarn dev
```

The app will be available at `http://localhost:3000` by default.

The dev server includes:
- Hot module replacement (changes reload automatically)
- Detailed error reporting
- Source maps for easier debugging

### Build for Production (Optional)

To test a production build locally:

```bash
npm run build
npm run start
```

---

## 🧪 Running Tests

```bash
# Run all tests
npm test

# Run tests in watch mode (re-runs on file change)
npm run test:watch

# Run tests with coverage report
npm run test:coverage
```

Tests are located alongside their source files in `__tests__/` directories, or as `.test.js` / `.spec.js` siblings.

> Before submitting a pull request, always run `npm test` and ensure all tests pass. See [CONTRIBUTING.md](CONTRIBUTING.md) for more.

---

## 🗂️ Project Structure Overview

```
roller-derby-coach-app/
├── drills/          # Drill library and practice plan builder
├── rules/           # WFTDA / USARS / JRDA rules reference
├── roster/          # Skater profiles and eligibility tracking
├── analytics/       # Bout statistics and performance metrics
├── ui/              # Shared front-end components and theming
└── docs/            # Documentation (you are here)
    ├── SETUP.md         # This file
    ├── CONTRIBUTING.md  # Contribution guidelines
    └── README.md        # Docs-level notes
```

For a full overview of each folder's purpose, see the root [README.md](../README.md).

---

## 🌐 Deployment

The app can be deployed to any Node.js-compatible hosting environment. Below are quickstart notes for common platforms.

### Self-Hosted / VPS

```bash
# Build the app
npm run build

# Start with a process manager (e.g. PM2)
npm install -g pm2
pm2 start npm --name "derby-coach" -- start
pm2 save
pm2 startup
```

### Vercel

```bash
npm install -g vercel
vercel
```

Follow the prompts. Set your environment variables in the Vercel dashboard under **Project Settings > Environment Variables**.

### Docker (Community-Supported)

A `Dockerfile` is planned for a future release. Community contributions to containerize the app are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 🔧 Troubleshooting

### `npm install` fails with peer dependency errors

Try:
```bash
npm install --legacy-peer-deps
```

### Port 3000 is already in use

Change the port in your `.env` file:
```
APP_PORT=3001
```

Or kill the process using the port:
```bash
# macOS / Linux
lsof -ti:3000 | xargs kill

# Windows (PowerShell)
Get-Process -Id (Get-NetTCPConnection -LocalPort 3000).OwningProcess | Stop-Process
```

### Database connection errors

- Double-check your `DATABASE_URL` in `.env`
- Make sure your database service is running
- Confirm the database exists and your user has the correct permissions

### Changes not reflecting after save

- Make sure the dev server is running (`npm run dev`)
- Hard-refresh your browser (`Ctrl+Shift+R` / `Cmd+Shift+R`)
- Check the terminal for build errors

---

## 🙋 Getting Help

If you’re stuck:

1. Check the [open issues](../../issues) to see if it’s a known problem
2. Search [closed issues](../../issues?q=is%3Aissue+is%3Aclosed) for prior solutions
3. Open a [new issue](../../issues/new) with a clear description and steps to reproduce
4. Tag it `setup` or `help wanted` so maintainers can find it quickly

We’re a friendly community — no question is too basic. Whether you’re a developer or a coach who’s never touched a terminal before, we’re happy to help you get rolling. 🛼

---

*Built with love for the roller derby community — WFTDA, USARS, and JRDA — by the StarPassForge collective.*
*Hit hard. Coach smart. Share freely.*
