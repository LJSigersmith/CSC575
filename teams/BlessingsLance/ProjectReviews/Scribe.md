# Project Review: Scribe-Android (scribe-org)

## Getting Started

### Documents

- **[CONTRIBUTING.md](https://github.com/scribe-org/Scribe-Android/blob/main/CONTRIBUTING.md)** — The primary contributor onboarding document. A 382-line guide organized with a linked table of contents covering: joining Matrix, finding beginner issues, dev environment setup, build variants, pre-commit hooks, testing conventions, bug reports, feature requests, PRs, data edits, localization, documentation, and design. Assessment: **Very clear** — comprehensive, friendly in tone, and well-structured for all levels.

- **[README.md](https://github.com/scribe-org/Scribe-Android)** — Project overview, feature descriptions, installation instructions, and links to all contribution resources. Includes quick-start clone/setup steps. Assessment: **Very clear** — concise and routes every audience correctly.

- **[ARCHITECTURE.md](https://github.com/scribe-org/Organization/blob/main/ARCHITECTURE.md)** — Organization-level document with Mermaid diagrams showing how all Scribe sub-projects (Android, iOS, Desktop, Data, Server, i18n) relate to each other and external systems (Wikidata, Wikipedia, Hugging Face, Unicode). Assessment: **Clear** — uniquely useful for understanding the data pipeline; helpful before touching any language data feature.

- **[Wikidata and Scribe Guide](https://github.com/scribe-org/Organization/blob/main/WIKIDATA_AND_SCRIBE_GUIDE.md)** — Explains what Wikidata is, how Scribe queries it via SPARQL, and why grammar data must be edited on Wikidata rather than directly in the repo. Assessment: **Clear** — important context for data-facing work; not required for pure Android UI contributions.

- **[Scribe Organization Projects Board](https://github.com/orgs/scribe-org/projects/1)** — Cross-repo roadmap tracking issues across all sub-projects by priority, status, and release milestone. Assessment: **Clear** — excellent overview of active and upcoming work.

### Code of Conduct

Scribe-Android publishes a `CODE_OF_CONDUCT.md` at [`.github/CODE_OF_CONDUCT.md`](https://github.com/scribe-org/Scribe-Android/blob/main/.github/CODE_OF_CONDUCT.md), based on the Contributor Covenant. It is referenced directly in CONTRIBUTING.md and acknowledged in every issue and PR template (contributors check a box: "I agree to follow Scribe-Android's Code of Conduct"). The code covers expected behavior (welcoming, respectful, collaborative), unacceptable behavior (harassment, derogatory language, trolling), and reporting procedures. This is a positive signal for community health and makes expectations explicit. Working in a project governed by this code would feel safe and professional — and notably, Scribe-Android is the only one of the four projects reviewed that has a formal, published code of conduct.

### User Installation

- **[Google Play Store](https://play.google.com/store/apps/details?id=be.scri.nde)** and **[F-Droid](https://f-droid.org/en/packages/be.scri.nde/)** — Scribe-Android is available through both major Android distribution channels. F-Droid availability signals the project's commitment to open-source values.

Assessment: **Trivial** — Standard app store install with no account, no setup, and no configuration required.

### Developer Installation

- **[CONTRIBUTING.md — Development Environment](https://github.com/scribe-org/Scribe-Android/blob/main/CONTRIBUTING.md)**

The setup process is: fork and clone the repo, open in Android Studio, run the app on a Pixel emulator (latest), and install pre-commit hooks (`pre-commit install && pre-commit run --all-files`). All language data is bundled as JSON assets in the repo — there is no external database, no Docker, and no backend server required to get started. The CONTRIBUTING.md notes that clearing the Android Studio cache via *File > Invalidate Caches* resolves most "changes not showing up" issues, and that emulators may occasionally need to be remade.

Assessment: **Easy** — The absence of a backend or containerized stack is a meaningful advantage over projects like CourtListener or wger. A developer with Android Studio already installed can have the app running in under 30 minutes. The only non-trivial element is the `InputMethodService` API (Android's keyboard extension framework), which is domain-specific and requires its own learning curve — but it is not required for most beginner issues.

### Organization

Assessment: **Super organized** — Each concern has a clear, documented home. CONTRIBUTING.md covers the development process. ARCHITECTURE.md covers system relationships. The Projects board tracks the cross-repo roadmap. Figma holds UI designs. Scribe-i18n handles localization via Weblate. Issue templates enforce consistent structure. There is no redundant or obviously stale documentation, and the separation of concerns across sub-repos is reflected clearly in the documentation rather than causing confusion.

### Summary

Getting started with Scribe-Android is among the most accessible experiences of any project reviewed. The CONTRIBUTING.md is explicit about welcoming people new to Kotlin, and it provides learning resource links for those just starting out. Dev setup is straightforward (no Docker, no external services). The issue pipeline is clearly labeled, and the Projects board gives an honest picture of active work. Documentation is complete, up to date, and written at an appropriate level for an intermediate Android developer. All signals indicate a community that has put real effort into onboarding.

---

## Community Communication

- **[Matrix — #ScribeAndroid Room](https://matrix.to/#/#ScribeAndroid:matrix.org)**
  - **Purpose:** Real-time developer chat specifically for Scribe-Android contributors. Used for setup questions, in-progress issue discussion, and direct access to the core team. CONTRIBUTING.md opens by directing all new contributors here first.
  - **Currency:** Active as of early 2025, consistent with ongoing commit activity and issue cross-references.
  - **Activity:** Estimated 5–15 messages/week; consistent with a small, tight-knit developer community.
  - **Responsiveness:** **Very likely** — The room is public and joinable without approval. Maintainer `andrewtavis` explicitly invites contributors and says *"We'd be happy to hear from you!"* Observed GitHub response patterns (hours to days) suggest similar responsiveness on Matrix.
  - **Response Time:** Likely within hours to one business day for technical questions.
  - **Content:** Warm and explicitly inclusive. The CONTRIBUTING.md encourages people to *"introduce yourself and tell us what your interests are if you're comfortable."* The Android-specific channel means questions won't get lost in cross-project noise.

- **[Matrix — General Room](https://matrix.to/#/!yQJjLmluvlkWttNhKo:matrix.org?via=matrix.org)**
  - **Purpose:** Organization-wide Scribe community space. Broader discussions spanning iOS, Android, Desktop, and Data sub-projects. Good for introductions and cross-cutting questions.
  - **Currency:** Active; referenced in all Scribe sub-project READMEs as the community entry point.
  - **Activity:** Estimated 10–20 messages/week across all Scribe contributors.
  - **Responsiveness:** **Very likely** — Same core team participates.
  - **Response Time:** Hours to one business day.
  - **Content:** Welcoming and community-building in tone. Appropriate for introductions or questions that span more than one sub-project.

- **[GitHub Issues](https://github.com/scribe-org/Scribe-Android/issues)**
  - **Purpose:** Formal tracker for bugs, features, and development tasks. Per CONTRIBUTING.md: *"the preferred channel for bug reports, features requests and submitting pull requests."* Every issue uses a structured template with a CoC acknowledgment checkbox.
  - **Currency:** Active — most recent batch opened February 26, 2025 (6+ issues by `angrezichatterbox` and `andrewtavis`).
  - **Activity:** ~2–5 new issues/month; consistent with a focused small-team project.
  - **Responsiveness:** **Very likely** — Maintainer `andrewtavis` responds to most issues. Example from Issue #149: *"I would love to work on this and am more than happy to help anyone fix this issue :)"* with 👍 and 🚀 emoji reactions.
  - **Response Time:** Hours to 2–3 days on labeled issues.
  - **Content:** Collaborative and constructive. Comments from `andrewtavis` and `angrezichatterbox` are technically clear and encouraging. Not terse or dismissive.

- **[Bi-Weekly Developer Syncs](https://github.com/scribe-org/Scribe-Android)**
  - **Purpose:** Recurring open video/call meetings for all contributors. Mentioned in CONTRIBUTING.md's first-steps section as something new contributors should *"consider joining."* Provides a synchronous touchpoint rare for a project this size.
  - **Currency:** Ongoing as of early 2025.
  - **Activity:** Every two weeks; includes core team and any active contributors.
  - **Responsiveness:** **Very likely** — Opt-in; simply join a meeting to get direct face time with maintainers.
  - **Response Time:** Every two weeks by structure.
  - **Content:** No public transcript available, but the existence of this channel is notable. It enables a new contributor to introduce themselves, ask architectural questions, and get feedback on in-progress work in a low-stakes synchronous setting.

### Summary

Scribe-Android's communication infrastructure is unusually strong for a project of its size. Matrix provides open, real-time access to the core team without an invitation barrier (unlike CourtListener's invite-only Slack). GitHub Issues is the formal async channel with consistently warm maintainer responses. Bi-weekly developer syncs offer a recurring synchronous touchpoint that most small open source projects don't have. The tone across all channels is genuinely welcoming. For a newcomer, this means you will never be stuck without a clear path to get help.

---

## Repositories

- **[scribe-org/Scribe-Android](https://github.com/scribe-org/Scribe-Android)**
  - **Purpose:** The main Android keyboard application — a pack of Android IME keyboards for language learners supporting translation (beta), verb conjugation, and word annotation. Fully offline; language data is bundled as static JSON sourced from Wikidata.
  - **Created:** 2022
  - **License:** GNU General Public License v3.0 (GPL-3.0)

- **[scribe-org/Scribe-Data](https://github.com/scribe-org/Scribe-Data)**
  - **Purpose:** A Python CLI tool that extracts and formats language data from Wikidata and Wikipedia using SPARQL queries. Produces the JSON data bundles consumed by all Scribe client apps. The data pipeline backbone of the entire organization.
  - **Created:** 2021
  - **License:** GNU General Public License v3.0 (GPL-3.0)

- **[scribe-org/Scribe-iOS](https://github.com/scribe-org/Scribe-iOS)**
  - **Purpose:** The more mature iOS/iPadOS keyboard application. Serves as the reference implementation for features being ported to Android (translation, conjugation, word annotation, dark/light mode). Actively used in App Store production.
  - **Created:** 2021
  - **License:** GNU General Public License v3.0 (GPL-3.0)

- **[scribe-org/Scribe-i18n](https://github.com/scribe-org/Scribe-i18n)**
  - **Purpose:** Centralized localization repository for all Scribe applications. Stores app UI strings as JSON files per language. Integrated into Scribe-Android as a git subtree and updated via Weblate (crowd translation platform). A non-code contribution path.
  - **Created:** 2023
  - **License:** GNU General Public License v3.0 (GPL-3.0)

- **[scribe-org/Organization](https://github.com/scribe-org/Organization)**
  - **Purpose:** Organization-level documentation: architecture diagrams, the Wikidata and Scribe Guide, branding/style guidelines, and cross-repo contributing information. The source of truth for understanding how all Scribe projects fit together.
  - **Created:** 2021
  - **License:** GNU General Public License v3.0 (GPL-3.0)

---

## Issue Tracking

- **[Scribe-Android Issue Tracker](https://github.com/scribe-org/Scribe-Android/issues)**
  - **Volume:** ~20–25 open issues (as of early March 2026; total issue/PR numbers have reached ~450+ including closed)
  - **Currency:**
    - Last Day: 0–1
    - Last Week: 0–2
    - Last Month: ~3–6 (February 2025 included a notable batch of 6+ new issues opened on Feb 26 alone)
    - Last 6 Months: ~15–25
  - **Activity:**
    - Last Day: 0–1
    - Last Week: 1–3
    - Last Month: ~5–10
    - Last 6 Months: ~20–30
  - **Beginner Issues:**
    - **Labels:** `good first issue`, `help wanted`, `design`, `-next release-`, `-priority-`, `hacktoberfest` (seasonal)
    - **Currency:**
      - Last Week: ~5–7 (batch opened Feb 26, 2025 by `angrezichatterbox` and `andrewtavis`)
      - Last Month: ~8–10
      - Last 6 Months: ~10–15
    - **Resolution:**
      - Last Week: 0–1
      - Last Month: 1–3
      - Last 6 Months: ~5–10
    - **Approachability:** Issues are well-written, clearly scoped, and include links to relevant Figma designs, related issues, and upstream code references. Issue #149 (Add translation source setting) is representative: it describes current behavior, desired behavior, references how similar functionality is already implemented in `SharedPreferences`, includes a visual mockup, and closes with *"I would love to work on this and am more than happy to help anyone fix this issue :)"* Issue #150 (Migrate Fragments to Jetpack Compose) includes a migration guide link, lists the affected files, and has maintainer emoji reactions. Issue #27 (Dark/light mode) has been open since 2022 — an example of why checking "blocked by" fields is important before picking up an issue. Comments across beginner issues are helpful and non-intimidating; maintainers consistently note they are happy to assist and review once a PR is opened.
    - **Summary:** The `good first issue` pipeline is one of the strongest across all projects reviewed. Issues are fresh (Feb 2025 batch), clearly written, cross-reference relevant code, include visual context, and have warm maintainer engagement. The main caution: always verify an issue is unblocked before starting, as some depend on upstream Scribe-Data or other in-progress work.

---

## Pull/Merge Requests

- **Volume:** ~3–5 open PRs (as of early March 2026)
- **Currency:**
  - Last Week: 0–1
  - Last Month: 1–3
  - Last 6 Months: ~5–10
- **Activity:**
  - Last Week: 0–1
  - Last Month: 1–3
  - Last 6 Months: ~5–10
- **Resolution:**
  - Last Week: 0–1 merged
  - Last Month: 1–3 merged
  - Last 6 Months: ~10–20 merged (visible in commit log: community PRs from `axif0` (Bangla localization), `yerimmii` (Korean), `OmarAI2003` (script fixes, README), `KesharwaniArpita` (Latin verbs in Scribe-Data), plus regular Weblate translation PRs)
- **Contributors:**
  - Last Month: ~2–4 (core team + 1–2 community contributors)
  - Last Year: ~10–20 distinct contributors across code and localization
- **New Contributors:**
  - Last Month: ~0–1
  - Last Year: ~5–10 first-time contributors (visible in commit history and outreach issue #62 discussion)
- **Summary:** PR volume is low but appropriate for a small early-stage project. External contributions are genuinely merged — the commit log shows real community PRs for features, localization, and bug fixes. There is no stalebot, and maintainer `andrewtavis` reviews PRs in a timely manner. The Weblate integration generates a steady stream of auto-merged translation PRs that keep the repository visibly active. The CONTRIBUTING.md's "ask first" guidance for significant feature work is standard and protects contributors from building something that won't be accepted. For a `good first issue` scoped task, the path from issue to merged PR is realistic within a semester timeline.

---

## Tools/Languages/Libraries/Frameworks

- **Tools:**
  - Android Studio — *used it*
  - Gradle (Kotlin DSL) — *used it*
  - GitHub Actions (CI) — *used it*
  - pre-commit (linting/formatting hooks) — *used it*
  - ADB / Android Emulator — *used it*
  - Weblate (crowd localization platform) — *heard of it*
  - Figma (UI design reference) — *heard of it*
  - SPARQL (Wikidata query language, used in Scribe-Data) — *unfamiliar*

- **Languages:**
  - Kotlin (~100% of Scribe-Android codebase) — *used it*
  - Python (Scribe-Data CLI; relevant only for data pipeline contributions) — *used it*
  - Shell — *used it*

- **Application Libraries/Frameworks:**
  - Android Jetpack (ViewModel, LiveData, Navigation, ViewPager2) — *used it*
  - Jetpack Compose (target UI migration from Fragments, active per Issue #150) — *used it*
  - InputMethodService (Android keyboard IME API — core to how Scribe keyboards work) — *unfamiliar*
  - SharedPreferences (settings persistence for keyboard options) — *used it*
  - JSON asset loading (language data bundled as static files) — *used it*
  - Hugging Face Transformers (translation beta feature, backend only) — *used it*

- **Testing Libraries/Frameworks:**
  - JUnit (unit tests in `src/test/java`) — *heard of it*
  - MockK (Kotlin-native mocking library, referenced in Issue #197) — *heard of it*
  - Android Instrumented Tests — *heard of it*
  - pre-commit / ktlint-style linting (automated on every commit) — *used it*

- **Summary:** The stack is an excellent fit overall. Kotlin is a primary language, Android Studio and Gradle are familiar tools, Jetpack and Compose are known, and GitHub Actions CI is familiar. The two meaningful unfamiliar areas are `InputMethodService` (the Android keyboard extension API, central to Scribe's core functionality, requiring dedicated documentation time) and MockK (a Kotlin-native mocking library, a modest learning curve). SPARQL and Figma are only relevant for specific contribution types. The active Jetpack Compose migration (Issue #150) is a beginner issue that directly aligns with modern Android development skills and would be an ideal first contribution.

---

## Assessment

Scribe-Android is the strongest candidate for a first open source contribution among all projects reviewed. Several factors make it stand out.

**What makes it compelling:** The community is explicitly built for onboarding. CONTRIBUTING.md invites people new to Kotlin by name and links learning resources. The Matrix chat is open to join without approval. Bi-weekly developer syncs provide direct synchronous access to maintainers — rare at this project size. The `good first issue` pipeline is the healthiest reviewed: labels are fresh (batch February 2025), issues are clearly scoped with design references and code pointers, and maintainers consistently offer assistance. The tech stack is a direct match — 100% Kotlin, familiar Jetpack components, Android Studio — with no language context-switching. Wikimedia affiliation and three consecutive years of GSoC participation demonstrate institutional commitment to mentoring contributors.

**What to be aware of:** The project is primarily maintained by `andrewtavis`, which means review timelines depend on one person's availability. Some issues are blocked by upstream Scribe-Data dependencies — the Projects board and "blocked by" labels should always be checked before starting work. `InputMethodService` is a domain-specific API not typically covered in Android development courses; it requires deliberate study but the maintainer has offered to help. The codebase is intentionally small, meaning contributions are visible and meaningful but the reviewer pool is thin.

**Concerns:** None that are disqualifying. The single-maintainer concentration is the primary structural risk, but it is mitigated by Wikimedia backing and GSoC mentorship history. The early-stage MVP nature of the Android app is actually an advantage for a contributor who wants to build something visible and real.

**Bottom line:** A well-scoped `good first issue` PR is achievable within a semester. The community is structured to support exactly this kind of contribution. The product — a privacy-respecting, Wikidata-powered keyboard for language learners — is something worth contributing to.

## Install Spike

### Developer Install Spike

- **Installation Documents**

- **Repository Links**

- **Summary**