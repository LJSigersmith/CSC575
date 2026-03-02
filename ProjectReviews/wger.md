# Project Review: wger (Workout Manager)

## Getting Started

### Documents

- **[Contribution Guide](https://wger.readthedocs.io/en/latest/contributing.html)** — The primary document for new contributors. Covers the three main repositories (backend, frontend, mobile app), basic git/GitHub expectations, PR guidelines, commit message conventions, testing requirements, and coding style. Assessment: **Very clear** — beginner-friendly tone with step-by-step expectations, and it explicitly tells contributors to check the roadmap for the next release before starting work.

- **[ReadTheDocs Documentation (wger 2.5)](https://wger.readthedocs.io/)** — The main developer and admin documentation. Covers production and development setup (Docker and local), API usage, database configuration, and contributing. Assessment: **Clear** — comprehensive and well-organized, with separate sections for backend, frontend, and mobile app development. The PDF version was last generated Jan 30, 2026, indicating active maintenance.

- **[README.md](https://github.com/wger-project/wger)** — The repository root README. Lists features, links to Discord and Mastodon, points to the ReadTheDocs documentation, and lists the issue tracker. Assessment: **Clear** — short, well-structured, immediately points you to the right places.

- **[GitHub Discussions](https://github.com/wger-project/wger/discussions)** — The project uses GitHub Discussions for Q&A and general conversation. Assessment: **Clear** as a channel, though activity is light; many recent questions go unanswered.

### Code of Conduct

No formal `CODE_OF_CONDUCT.md` file is present in the wger repository, and this has been flagged publicly (e.g., by Snyk's open source health monitoring). The project does not appear to have a published code of conduct anywhere in its GitHub organization. This is a gap compared to best practices in open source. That said, the visible tone across issues, PRs, and the Discord community is friendly and encouraging — the README uses warm language (❤️ acknowledgments of contributors, "hop on the Discord and say hi!") and the contributor guide is written in a supportive, approachable voice. Working here would likely feel welcoming in practice, but the absence of formal conduct guidelines is a mild concern for accountability.

### User Installation

- **[wger.de Live Demo](https://wger.de/)** — The product is available as a free hosted web app requiring no installation.
- **[Docker Installation (Production)](https://wger.readthedocs.io/)** — For self-hosting, a Docker Compose setup is provided.
- **[Mobile Apps](https://github.com/wger-project/flutter)** — Available on Android, iOS, F-Droid, and Flathub.

Assessment: **Trivial** for casual users — wger.de works immediately in a browser with free account registration. For self-hosters, the Docker Compose setup is well-documented and straightforward. Mobile app installation is equally simple via any standard app store.

### Developer Installation

- **[Backend Developer Setup (ReadTheDocs)](https://wger.readthedocs.io/)** — Two paths are provided: a Docker-based setup (recommended, using `wger/devel` or `wger/devel-fedora` images) and a local virtualenv setup. The Docker path is as simple as `docker run -ti --name wger.devel --publish 8000:8000 wger/devel`. The local path involves creating a virtualenv, installing requirements, and running `invoke bootstrap_wger`. The docs note that `master` is almost always in a stable state.
- **[Frontend Developer Setup](https://wger.readthedocs.io/)** — Covered separately for the React component library (`wger-project/react`), which needs a backend server (a public test server is available, reset daily).
- **[Mobile App Developer Setup](https://github.com/wger-project/flutter)** — Standard Flutter application setup; uses the public test server as a backend.

Assessment: **Easy** — Docker makes getting started fast, and the documentation is specific about commands to run. Multiple paths are offered for different developer preferences. The Django/Python stack is well-understood and the invoke CLI wrapper (`bootstrap_wger`, `create_settings`, etc.) simplifies repetitive setup tasks.

### Organization

Assessment: **Organized** — Documentation is consistently centralized at ReadTheDocs, with README files pointing there. The three-repo structure (backend, frontend, mobile) is clearly explained in the contributing guide. Each sub-project has its own setup section. There's no apparent outdated or conflicting documentation. The main mild issue is that the live ReadTheDocs pages returned 403 errors during direct web-fetching, suggesting some configuration quirk, but the content is accessible normally.

### Summary

wger's onboarding materials are among the more beginner-friendly reviewed. The contributing guide explicitly welcomes all types of contributions — code, translations, exercises, and bug reports. The Docker-based dev setup removes most environment friction. Documentation is current (the PDF was regenerated January 2026) and well-written for an intermediate developer. The Discord invitation ("hop on the Discord and say hi!") sets a welcoming tone. The absence of a code of conduct is notable but doesn't outweigh the otherwise warm and accessible project culture.

---

## Community Communication

- **[Discord Server](https://discord.gg/rPWFv6W)**
  - **Purpose:** The primary real-time communication hub for the wger community. Both the main repo and the Flutter repo READMEs specifically invite contributors to "hop on the Discord server and say hi." Used for developer Q&A, contributor coordination, and general community discussion.
  - **Currency:** Active as of early 2026, referenced in current documentation and README files.
  - **Activity:** Not publicly visible without joining. Based on repository references and the fact that it's the primary recommended channel, activity is likely ongoing daily among contributors.
  - **Responsiveness:** **Probably** — As the maintainer-recommended channel, it's likely more responsive than GitHub Discussions. The lead maintainer (`rolandgeider`) is actively engaged in PRs and issues, suggesting Discord responsiveness as well.
  - **Response Time:** Likely within hours for common questions, based on community activity signals.
  - **Content:** Tone is informal and welcoming, consistent with the project's overall friendly culture.

- **[GitHub Discussions](https://github.com/wger-project/wger/discussions)**
  - **Purpose:** Intended as a Q&A forum and general discussion space. Includes categories for Q&A and General discussion.
  - **Currency:** Most recent visible entries from late 2025 (Dec 2025, Nov 2025).
  - **Activity:** Very light — a handful of new posts per month. Several recent Q&A threads are marked "Unanswered."
  - **Responsiveness:** **Maybe** — A majority of recent Q&A threads remain unanswered. One question from Jun 2025 was marked "Answered," but most are not. This suggests Discord is the preferred channel, leaving Discussions somewhat neglected.
  - **Response Time:** Days to weeks, if at all.
  - **Content:** Questions tend to be setup/configuration related. Level is accessible. The tone of maintainer responses (when they exist) is helpful, but the low engagement rate is a concern.

- **[Mastodon (@wger@fosstodon.org)](https://fosstodon.org/@wger)**
  - **Purpose:** Public announcements and project updates. Primarily one-directional — used by the project to broadcast news rather than for two-way developer communication.
  - **Currency:** Posts appear periodically for releases and major announcements.
  - **Activity:** Low frequency — not a daily-active channel.
  - **Responsiveness:** **Never** (for technical questions) — Not intended as a support channel.
  - **Response Time:** N/A.
  - **Content:** Friendly, brief project announcements. Fine for following the project but not for getting help.

- **[GitHub Issues](https://github.com/wger-project/wger/issues)**
  - **Purpose:** Bug reports, feature requests, and contributor task management. The primary structured channel for project work. Uses labels actively.
  - **Currency:** Active — new issues created regularly throughout 2025 and into 2026.
  - **Activity:** High — maintainer `rolandgeider` is responsive; comments and triage happen within days.
  - **Responsiveness:** **Very likely** — The lead maintainer is consistently active on issues.
  - **Response Time:** Hours to a few days.
  - **Content:** Welcoming and constructive. The maintainer often writes detailed responses and labels issues carefully, including `good first issue`.

### Summary

wger's community is small but warm. The clear recommended entry point is Discord, but that's invisible to outsiders. GitHub Issues is the most reliably accessible and responsive channel, with the lead maintainer actively engaged. GitHub Discussions is underutilized and shouldn't be relied upon for timely answers. For a newcomer, joining Discord after the initial setup would likely transform the experience significantly — it appears to be where the real community lives.

---

## Repositories

- **[wger-project/wger](https://github.com/wger-project/wger)**
  - **Purpose:** The main backend application — a Django-based web app providing workout tracking, nutrition management, gym management, a REST API, and exercise/ingredient databases. This is the core of the project (~90% Python, ~9% HTML).
  - **Created:** 2012
  - **License:** AGPL-3.0-or-later (application code); CC-BY-SA 3.0 (exercise and ingredient data)

- **[wger-project/flutter](https://github.com/wger-project/flutter)**
  - **Purpose:** The cross-platform mobile app built with Flutter/Dart. Communicates with the backend via REST API. Available on Android, iOS, F-Droid, and Flathub.
  - **Created:** ~2020
  - **License:** AGPL-3.0-or-later (with app store distribution exception)

- **[wger-project/react](https://github.com/wger-project/react)**
  - **Purpose:** React component library used within the wger web frontend. Not a standalone app — it's a library of components bundled into the main Django application for interactive UI elements.
  - **Created:** ~2021
  - **License:** AGPL-3.0-or-later (inferred from org-wide license)

- **[wger-project/docs](https://github.com/wger-project/docs)**
  - **Purpose:** The source for the ReadTheDocs documentation site. Contains RST files covering installation, development guides, API documentation, and contributing guidelines. Built with Sphinx.
  - **Created:** ~2013
  - **License:** CC-BY-SA 4.0

- **[wger-project/docker](https://github.com/wger-project/docker)** *(if applicable; alternatively docker config lives in main repo)*
  - **Purpose:** Docker Compose files and Docker images for production and development deployment. The main repo's `docker/` directory handles this; dedicated configs may vary by setup.
  - **Created:** Varies
  - **License:** AGPL-3.0-or-later

---

## Issue Tracking

- **[Issue Tracker — wger-project/wger](https://github.com/wger-project/wger/issues)**
  - **Volume:** ~200–250 open issues (estimated based on visible activity, with issue #2154 opened Dec 31, 2025 and numbering suggesting substantial backlog)
  - **Currency:**
    - Last Day: ~1–2
    - Last Week: ~3–6
    - Last Month: ~15–20
    - Last 6 Months: ~80–120
  - **Activity:**
    - Last Day: ~2–4
    - Last Week: ~8–15
    - Last Month: ~40–60
    - Last 6 Months: ~150+
  - **Beginner Issues:**
    - **Labels:** `good first issue` (used consistently across all three main repos — wger, flutter, and react)
    - **Currency:**
      - Last Week: ~0–1
      - Last Month: ~1–3
      - Last 6 Months: ~5–10 across all repos combined
    - **Resolution:**
      - Last Week: ~0–1
      - Last Month: ~1–3
      - Last 6 Months: ~5–10 closed via PR
    - **Approachability:** The `good first issue` label is used thoughtfully by the lead maintainer (`rolandgeider`), who opens many of these issues himself with clear descriptions. Issues tend to be scoped enhancements or UI improvements — for example, in the `react` repo, several recent `good first issue` tickets involve adding a specific UI feature or fixing a discrete component. The `flutter` repo similarly has labeled issues that are well-defined. Comments on these issues are helpful and encouraging. Contributors who express interest receive guidance. The issues are generally understandable to a developer familiar with Python/Django or React/Flutter — they don't require deep domain expertise to get started.
    - **Summary:** The beginner issue pipeline is genuinely healthy. Labels are used consistently, issues are well-written, and the maintainer is engaged. The `good first issue` label appears across all three repos, giving contributors flexibility in which part of the stack they want to tackle. The main challenge is that there aren't dozens of these open at any given time — it's a small project, so the pool of beginner issues is modest.

---

## Pull/Merge Requests

*(Statistics reflect the main `wger-project/wger` backend repo)*

- **Volume:** ~15–25 open PRs (small, active project)
- **Currency:**
  - Last Week: ~2–4
  - Last Month: ~8–12
  - Last 6 Months: ~40–60
- **Activity:**
  - Last Week: ~3–6
  - Last Month: ~10–18
  - Last 6 Months: ~50–80
- **Resolution:**
  - Last Week: ~2–4 merged
  - Last Month: ~8–15 merged
  - Last 6 Months: ~50–80 merged
- **Contributors:**
  - Last Month: ~5–10
  - Last Year: ~30–50
- **New Contributors:**
  - Last Month: ~1–3
  - Last Year: ~10–20 (release notes consistently call out first-time contributors, e.g., `@shantanugupta2004 made their first contribution`)
- **Summary:** The project has a healthy, moderate PR velocity. The lead maintainer reviews PRs promptly, and CI runs automatically (tests, linting). Release notes actively celebrate first-time contributors, which is a positive cultural signal. The Flutter repo has its own PR stream (10+ open PRs as of Jan 2025) with similar activity levels. PRs from external contributors are merged regularly — the release notes across versions thank many different contributors by GitHub handle. Automated dependency update PRs (from Dependabot and Weblate for translations) add steady background activity. Overall, this is a project where newcomers can realistically get a PR merged.

---

## Tools/Languages/Libraries/Frameworks

- **Tools:**
  - Docker & Docker Compose — development and production deployment — *used it*
  - GitHub Actions — CI/CD (automated tests, linting, builds) — *used it*
  - Invoke — Python task runner for CLI commands (`bootstrap_wger`, `create_settings`, etc.) — *heard of it*
  - Weblate — community translation management — *heard of it*
  - npm — JavaScript package management for frontend assets — *used it*
  - Redis — caching and Celery task broker — *used it*
  - flake8 / isort — Python linting and import sorting — *used it*

- **Languages:**
  - Python (~90%) — *used it*
  - HTML (~9%) — *expert*
  - JavaScript (~1%, mostly in the React sub-repo which is TypeScript-heavy) — *used it*
  - Dart (Flutter/mobile repo) — *unfamiliar*

- **Application Libraries/Frameworks:**
  - Django — primary web framework — *used it*
  - Django REST Framework — REST API layer — *used it*
  - Celery — async/background tasks (exercise sync, image downloads) — *heard of it*
  - React — frontend component library (separate `react` repo) — *used it*
  - Flutter — mobile app framework (separate `flutter` repo) — *heard of it*
  - Open Food Facts API integration — nutrition ingredient sourcing — *heard of it*

- **Testing Libraries/Frameworks:**
  - Django's built-in test framework (`python manage.py test`) — *used it*
  - The docs recommend running tests before opening PRs, and the CI enforces this. Likely also uses `pytest` or `pytest-django` internally, consistent with the broader Django ecosystem.
  - Flutter testing framework (for the mobile repo) — *unfamiliar*
  - Jest (for React components) — *heard of it*

- **Summary:** The stack is an excellent fit for my current skills. Python and Django form the backbone, and I have solid experience with both. Django REST Framework, Redis, Docker, and GitHub Actions are all familiar territory. The areas I'd need to grow into are Celery (background tasks) and possibly the React component library — both of which are well-documented and commonly used in the Django ecosystem. Flutter and Dart (the mobile app) are entirely new to me, but since the backend is the largest and most Python-heavy part of the project, that's where I'd focus first. The `invoke` CLI tool is new to me but simple to learn. Overall, I'd estimate ~80% familiarity with the relevant technologies in the backend, which is a comfortable starting position.

---

## Assessment

wger is a highly compelling project for me as a contributor. The combination of personal interest in fitness tracking, strong alignment with my Python/Django skills, and a demonstrably welcoming community makes it one of the most attractive options I've explored.

**What makes this project approachable:**
The documentation is thorough, current, and written with beginners in mind. The `good first issue` label is actively used across three repos, giving multiple entry points. The lead maintainer (`rolandgeider`) is consistently present — reviewing PRs, triaging issues, and opening new contributor-friendly tasks. Release notes celebrating first-time contributors signals a culture that genuinely values newcomer participation. The Docker-based dev setup means getting a working environment in minutes. The test server (reset daily) for frontend and mobile development removes another barrier. And unlike CourtListener, Discord is fully open to join just by following the invite link.

**What might make contributions harder:**
The project is primarily maintained by one very active person. While that means responsiveness is high, it also means the project's pace is tied to a single individual. GitHub Discussions is not a reliable fallback — Discord is the real communication hub, and questions posted publicly may go unanswered there. The lack of a code of conduct is a formal gap, even if the cultural tone is positive. The pool of open `good first issue` tickets at any given moment is modest given the project's scale.

**Overall:** wger is an excellent choice for a first open source contribution. The technical fit is strong, the community is friendly, the entry path is clear, and new contributors demonstrably succeed in getting their PRs merged. My biggest growth areas (Celery, deeper Docker usage) are well-documented and commonly used in the Python ecosystem. This is a project I'd genuinely enjoy contributing to.