<p align="center"><a href="https://metacall.io/" target="_blank"><img src="https://github.com/metacall.png" width="28%"></a></p>

<h1 align="center"><b>MetaCall Launchpad</b></h1>

<p align="center">The official web-based dashboard for managing and deploying polyglot applications to the MetaCall FaaS platform.</p>

<br>

<p align="center">
  <a href="https://github.com/metacall/core/discussions"><img src="https://img.shields.io/badge/GitHub-Discussions-333?logo=github" alt="GitHub Discussions"></a>
  <a href="https://twitter.com/metacallio"><img src="https://img.shields.io/badge/Twitter-@metacallio-1DA1F2?logo=twitter&logoColor=white" alt="Twitter"></a>
  <a href="https://discord.gg/upwP4mwJWa"><img src="https://img.shields.io/badge/Discord-Join%20Server-5865F2?logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://t.me/joinchat/BMSVbBatp0Vi4s5l4VgUgg"><img src="https://img.shields.io/badge/Telegram-Join%20Group-26A5E4?logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="https://matrix.to/#/#metacall:matrix.org"><img src="https://img.shields.io/badge/Matrix-Join%20Room-0DBD8B?logo=matrix&logoColor=white" alt="Matrix"></a>
</p>

<br>

## Table of Contents

- [About](#about)
- [See It in Action](#see-it-in-action)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Commands Reference](#commands-reference)
- [Contributing](#contributing)
- [License](#license)

## About

MetaCall Launchpad is the official web-based interface for managing and deploying polyglot applications to the MetaCall Function-as-a-Service (FaaS) platform. It allows developers to configure environments, inspect active deployments, monitor real-time logs, and invoke polyglot functions directly from the browser.

This project is built with:
- **[React](https://react.dev/)** + **[TypeScript](https://www.typescriptlang.org/)** — Core UI framework
- **[Vite](https://vitejs.dev/)** — Build tooling and dev server
- **[Tailwind CSS](https://tailwindcss.com/)** — Styling framework
- **[Vitest](https://vitest.dev/)** — Unit testing
- **[Playwright](https://playwright.dev/)** — End-to-end testing

## See It in Action

A complete walk-through of the primary developer workflow — deployment management, real-time logs, and polyglot function execution:

<p align="center">
  <video src="https://github.com/user-attachments/assets/123bdb2c-f7a6-4530-a8a0-c0726e29cd68" width="640" autoplay loop muted playsinline>
    <a href="https://github.com/user-attachments/assets/123bdb2c-f7a6-4530-a8a0-c0726e29cd68">Watch the Launchpad Demonstration Video</a>
  </video>
</p>

## Key Features

* **Authentication & Access Control**: Secure login, registration, token-based authorization, and protected client-side routing.
* **Polyglot Service Deployment**: Deploy applications directly from ZIP files, remote Git repositories, or pre-configured software templates.
* **Interactive Function Testing**: Inspect deployed endpoints and invoke functions written in different programming languages (JavaScript, Python, Ruby, Go, C#, C/C++, Rust, etc.) in real time.
* **Real-Time Logs**: Stream live stdout and stderr consoles from deployed services for simplified debugging and performance monitoring.
* **Subscription Management**: Review and update subscription tiers, purchase or manage licenses, and checkout billing statements.
* **Settings & Live Support**: Manage API tokens, configure account preferences, and contact the MetaCall support team.

## Getting Started

### Prerequisites

* **Node.js**: Version 20.0.0 or higher
* **npm**: Version 10.0.0 or higher
* **MetaCall FaaS Backend**: A running instance of the MetaCall FaaS server (defaults to `http://localhost:9000`)

### Run Locally

1. Fork the repository by clicking **Fork** on the top right of the main repository.
2. Clone your fork:
   ```bash
   git clone https://github.com/<your-username>/dashboard.git
   cd Dashboard
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Configure your environment:
   ```bash
   cp .env.example .env
   ```
   Set `VITE_FAAS_URL` to point to your running FaaS backend.
5. Start the local development server:
   ```bash
   npm run dev
   ```
   Access the live development server at `http://localhost:5173`.

## Project Structure

```
Dashboard/
├── .github/                  # GitHub workflows, PR & issue templates
├── public/                   # Static assets (logos, loaders, demo video)
├── src/
│   ├── app/                  # App-level configuration (router, providers)
│   ├── assets/               # Imported assets (images, SVGs)
│   ├── features/             # Feature modules (each is self-contained)
│   │   ├── auth/             # Authentication & login
│   │   ├── chat/             # Live support chat
│   │   ├── dashboard/        # Main dashboard view
│   │   ├── deployments/      # Deployment management (ZIP, Git, templates)
│   │   ├── logs/             # Real-time log streaming
│   │   ├── plan/             # Subscription & billing
│   │   └── settings/         # User settings & API tokens
│   ├── lib/                  # Utility libraries & helpers
│   ├── pages/                # Route-level page components
│   ├── services/             # API service layer (FaaS communication)
│   ├── shared/               # Shared UI components, types, constants
│   │   ├── ui/               # Reusable UI components
│   │   ├── layout/           # Layout components (sidebar, header)
│   │   ├── types/            # Shared TypeScript types
│   │   └── constants/        # App-wide constants
│   └── styles/               # Global styles & Tailwind config
├── tests/                    # Playwright E2E tests
│   ├── e2e/                  # End-to-end test specs
│   ├── fixtures/             # Test fixtures & helpers
│   ├── mocks/                # Mock data for tests
│   └── pages/                # Page Object Models
├── vite.config.ts            # Vite configuration
├── playwright.config.ts      # Playwright configuration
└── package.json              # Dependencies & scripts
```

## Commands Reference

| Command | Description |
|---|---|
| `npm run dev` | Start the local development server |
| `npm run build` | Build the production application bundle |
| `npm run preview` | Preview the local production build |
| `npm run lint` / `lint:fix` | Check and fix ESLint issues |
| `npm run format` / `format:check` | Format files and check formatting with Prettier |
| `npm run unit` | Run unit tests with Vitest |
| `npm run test` | Run full Playwright E2E suite |
| `npm run test:smoke` | Run fast Playwright E2E smoke tests |

For detailed information about tests and E2E setup, refer to the [Testing Guide](TEST_README.md).

## Contributing

We are thrilled to welcome contributions from our community! Whether you are squashing a bug, proposing an exciting new feature, or submitting a pull request, your help is incredibly valuable to us.

Please check out our [Contributing Guidelines](CONTRIBUTING.md) to see how you can get started, set up your development environment, and submit your work. If you encounter any issues, please feel free to open one!

## Code of Conduct

To ensure a positive and inclusive environment, please review our [Code of Conduct](https://github.com/metacall/.github/blob/master/CODE_OF_CONDUCT.md).

## License

A license has not been specified for this project yet and will be added in a future release.
