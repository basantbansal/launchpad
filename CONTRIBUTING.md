# Welcome to MetaCall Launchpad

We're excited to have you join our community and contribute to making MetaCall Launchpad better. Please follow this guide to ensure a smooth contribution process and maintain the quality of our codebase.

Before diving into the code, we highly recommend checking out these videos to get a full picture of the Launchpad and how it works:
- [MetaCall Launchpad Overview](https://www.youtube.com/watch?v=2RAqTmQAWEc)
- [How to create a Newsletter self-contained solution with MetaCall & DynamoDB](https://www.youtube.com/watch?v=yo3eJmje_A8)

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Our Development Process](#our-development-process)
- [Contribution Flow](#contribution-flow)
- [Issues](#issues)
- [Pull Requests](#pull-requests)
- [Conventional Commits](#conventional-commits)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Testing](#testing)

## Code of Conduct

This project and everyone participating in it is governed by the [MetaCall Code of Conduct](https://github.com/metacall/.github/blob/master/CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please read the full text to understand the expected behavior.

## Our Development Process

We use GitHub to host code, track issues and feature requests, and accept pull requests. All changes happen through pull requests — they are the best way to propose changes to the codebase.

## Contribution Flow

We openly accept contributions of all kinds — no gatekeeping, no restrictions. Here's how a typical contribution looks for this project:

```
    ┌───────────────────────────┐
    │  Find something to work   │
    │  on: a bug, a feature,    │
    │  a UI improvement, or     │
    │  a documentation gap      │
    └─────────────┬─────────────┘
                  │
                  ▼
    ┌───────────────────────────┐
    │  Open an issue describing │
    │  the problem or idea      │
    │  (skip for small typos    │
    │   or obvious fixes)       │
    └─────────────┬─────────────┘
                  │
                  ▼
    ┌───────────────────────────┐
    │  Fork, code, and open a   │
    │  Pull Request linking     │
    │  your issue               │
    └─────────────┬─────────────┘
                  │
                  ▼
    ┌───────────────────────────┐
    │  A maintainer reviews     │
    │  your PR, provides        │
    │  feedback, and merges it  │
    └───────────────────────────┘
```

Here are some areas where the Launchpad could use your help:
- **UI/UX improvements** — Polish the dashboard, improve responsiveness, or enhance accessibility.
- **Deployment features** — Improve the ZIP/Git deploy flows or the real-time log streaming.
- **Testing** — Add unit tests (Vitest) or E2E tests (Playwright) for uncovered areas.
- **Documentation** — Fix typos, clarify setup instructions, or add missing guides.

 **Tip:** If you're planning to add a new feature, we'd love to hear about it first! Come chat with us on [Discord](https://discord.gg/upwP4mwJWa) so we can discuss the idea together before you start coding.
## Issues

Open an issue **only** if you want to report a bug or request a feature. Please use our issue templates, which provide hints on what information we need to help you out.

- **Don't open issues for general questions or support.** Instead, join our community channels listed in the [README](README.md#community).
- **Search existing issues first** to avoid duplicates.
- If you find an existing issue that describes your problem, add a 👍 reaction instead of opening a new one.

## Pull Requests

**Please open an issue before starting a Pull Request** unless it's a typo or a really obvious fix. A PR may be rejected if no issue was created first to discuss the need for the change.

1. **Fork the repository** and create your branch from `main`.
2. If you've added code that should be tested, **add tests**.
3. If you've changed APIs or features, **mention the change in the PR description**.
4. Ensure the test suite passes (`npm run unit` and `npm run test`).
5. Make sure your code lints and is formatted (`npm run lint` and `npm run format`).
6. Submit your pull request!

## Conventional Commits

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification. Pull request titles should follow this format:

| Prefix       | Use when...                                         |
|--------------|-----------------------------------------------------|
| `fix:`       | The PR is a bug fix                                 |
| `feat:`      | The PR introduces a new feature                     |
| `docs:`      | The PR only relates to documentation                |
| `chore:`     | The PR is related to cleanup, CI, or tooling        |
| `test:`      | The PR is only related to tests                     |
| `refactor:`  | The PR is a code refactor with no behavior change   |

> **Tip:** The title must also be clear and descriptive, using the **imperative mood** (e.g., `fix: resolve login redirect loop`).

## Development Setup

To set up the project locally:

1. **Clone your fork:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/dashboard.git
   cd Dashboard
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Configure environment:**
   ```bash
   cp .env.example .env
   ```
   Set `VITE_FAAS_URL` to point to your running MetaCall FaaS backend.
4. **Start development server:**
   ```bash
   npm run dev
   ```

For more details, refer to the [Testing Guide](TEST_README.md) and [README](README.md).

## Coding Standards

- We use **ESLint** for linting and **Prettier** for code formatting.
- Always run `npm run lint:fix` and `npm run format` before committing.
- Write clean, readable, and well-documented code.
- Use meaningful commit messages following [Conventional Commits](#conventional-commits).

## Testing

Before submitting a pull request, ensure all tests pass:

| Command          | Description                  |
|------------------|------------------------------|
| `npm run unit`   | Run unit tests with Vitest   |
| `npm run test`   | Run Playwright E2E tests     |

If you add new features or fix bugs, please include corresponding tests.

---

Happy contributing! Your efforts help make MetaCall better for everyone.
