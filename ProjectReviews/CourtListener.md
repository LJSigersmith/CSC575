# Project Review: CourtListener (Free Law Project)

## Getting Started

### Documents

- **[Getting Started Developing CourtListener (Wiki)](https://github.com/freelawproject/courtlistener/wiki/Getting-Started-Developing-CourtListener)** — The primary developer onboarding document. Covers architecture, Docker-based dev environment setup, AWS resource access, CI/CD pipeline overview, PR guidelines, and production monitoring. Recently updated (Feb 24, 2026). Assessment: **Very clear** — well-structured and comprehensive for a newcomer developer.

- **[README.md](https://github.com/freelawproject/courtlistener)** — The repository root README gives a high-level project overview, describes the folder structure (cl/, `docker/`, `scripts/`), links to the volunteer page, and points to the developer wiki. Assessment: **Clear** — good entry point to orient yourself.

- **[Volunteer/Contribute Page](https://free.law/volunteer)** — Describes multiple ways to contribute (code, research, legal, advocacy). Links to a project board for volunteer developers. Assessment: **Clear** — welcoming and practically useful.

- **[CourtListener FAQ](https://www.courtlistener.com/faq/)** — User-facing FAQ covering how to get involved, what the site covers, and contact info. Mentions GitHub and Slack as the main planning channels. Assessment: **Clear**.

- **[GitHub Discussions](https://github.com/freelawproject/courtlistener/discussions)** — Q&A forum for the project. The wiki specifically encourages asking questions here rather than Slack so answers are preserved. Assessment: **Clear**, though activity is light.

### Code of Conduct

The CourtListener repository does not appear to publish a standalone `CODE_OF_CONDUCT.md` in the repository itself. The GitHub organization page does not prominently feature one either. The repository links to [GitHub's community guidelines](https://github.com/freelawproject/courtlistener/discussions) as part of its Discussions forum. This is a noticeable gap compared to many open source projects. Without a formal code of conduct, it's harder to know exactly what standards of behavior are expected, though the tone in existing issues and communications appears professional and collegial.

### User Installation

- **[CourtListener.com](https://www.courtlistener.com/)** — The product is a live hosted web application requiring no installation. Users simply visit the site and can search case law, opinions, oral arguments, dockets, and judge information for free.

Assessment: **Trivial** — There is nothing to install. The product is fully accessible online at no cost. Even the API is publicly accessible with a free account.

### Developer Installation

- **[Getting Started Developing CourtListener (Wiki)](https://github.com/freelawproject/courtlistener/wiki/Getting-Started-Developing-CourtListener)**

The developer setup relies on Docker and Docker Compose to spin up all required services (PostgreSQL, Redis, Celery, Elasticsearch, Django, etc.). The wiki walks through cloning the repo, running `docker compose up`, and explains the project's architecture components. A contributor license agreement (CLA) is required for first-time contributors (handled automatically by a bot on your first PR).

Assessment: **Reasonable** — Docker simplifies setup considerably, but the stack is non-trivial: PostgreSQL, Redis, Celery, Elasticsearch, and Django must all come up correctly together. Some AWS resource access is also needed for certain features. A developer comfortable with Docker should be able to get up and running within a few hours, but troubleshooting could be time-consuming.

### Organization

Assessment: **Organized** — The primary documentation lives in a GitHub Wiki with well-named pages. The README provides a clear map to those resources. The volunteer page and contributing guidance are easy to find. One mild downside is that some Q&A knowledge lives in Slack and doesn't get preserved publicly, which the maintainers acknowledge and are trying to address by encouraging GitHub Discussions use. No obvious redundant or out-of-date documentation was found.

### Summary

Getting started with CourtListener is reasonably well-supported. The developer wiki is thorough and recently maintained (last edited Feb 2026). The project explicitly welcomes volunteers, provides a project board for contributors to pick up work, and has a CLA bot to streamline the legal side. The documentation is written at a level appropriate for an intermediate developer familiar with Python/Django web apps. The lack of a formal code of conduct is a minor concern, but the tone across issues and communications suggests a welcoming environment. Overall, this project sends positive signals to newcomers.

---

## Community Communication

- **[Slack Workspace (Free Law Project)](https://www.courtlistener.com/contribute/)**
  - **Purpose:** The primary real-time communication channel for developers and volunteers. Used for general discussion, quick Q&A, coordination between contributors, and announcements. The wiki and FAQ both reference it as the main place developers congregate. Channels include `#librarians` for research volunteers and `#flp-general-chat` for general discussion.
  - **Currency:** Referenced as actively used as of 2025–2026 in project documentation. The wiki notes that questions answered in Slack are "lost in a black hole," implying ongoing active use.
  - **Activity:** Not publicly visible without an invitation. Based on project documentation references, it appears active (multiple channels, ongoing discussions referenced in issues).
  - **Responsiveness:** **Probably** — Maintainers and regular contributors appear to be on Slack regularly, based on how frequently it's referenced. Response times for direct questions are likely fast during business hours.
  - **Response Time:** Likely within hours for technical questions, based on the community's apparent activity level.
  - **Content:** Tone appears informal and collegial based on Slack conversation excerpts referenced in GitHub issues (e.g., the F.Cas. discussion in issue #689 cites a Slack conversation). Technical but approachable.

- **[GitHub Discussions](https://github.com/freelawproject/courtlistener/discussions)**
  - **Purpose:** Intended as the persistent, searchable Q&A and discussion forum for developers and users. The developer wiki explicitly encourages using this over Slack so answers can be found later.
  - **Currency:** Most recent discussions visible from late 2025 (e.g., questions from Nov 2025).
  - **Activity:** Light — roughly 1–3 new discussions per month based on visible activity. Many questions appear to go unanswered.
  - **Responsiveness:** **Maybe** — Some questions receive responses, but several recent ones (Nov 2025) are marked "Unanswered." Engagement is inconsistent.
  - **Response Time:** Days to weeks for responses, or no response.
  - **Content:** Questions tend to be technical (API usage, data interpretation) and at an intermediate level. Tone from maintainers is helpful when they do respond.

- **[GitHub Issues](https://github.com/freelawproject/courtlistener/issues)**
  - **Purpose:** Bug reports, feature requests, and project planning. Issues are assigned to contributors and serve as the primary task-tracking mechanism.
  - **Currency:** Active — new issues created regularly (multiple per week based on observed activity).
  - **Activity:** High — maintainers and contributors comment frequently on open issues.
  - **Responsiveness:** **Very likely** — Maintainers are responsive on issues, especially for bugs and assigned work.
  - **Response Time:** Hours to a few days.
  - **Content:** Technical and direct. Tone is professional. Maintainers are helpful and encourage contributors to chime in.

### Summary

The community has two distinct tiers: Slack (active, real-time, but closed/invisible to outsiders) and GitHub (open, but Discussions are lightly used). GitHub Issues is the most reliably responsive channel. If you joined Slack you'd likely get fast answers, but the barrier to entry is getting an invitation. For a newcomer, the best strategy is to engage via GitHub Issues and Discussions, and seek a Slack invite via the volunteer signup form. The community appears welcoming and technically competent, though small.

---

## Repositories

- **[freelawproject/courtlistener](https://github.com/freelawproject/courtlistener)**
  - **Purpose:** The main CourtListener web application — a Django-based platform providing search, browsing, alerts, and API access for all court data (opinions, dockets, judges, oral arguments, financial disclosures).
  - **Created:** 2010
  - **License:** GNU Affero General Public License v3 (AGPL-3.0)

- **[freelawproject/juriscraper](https://github.com/freelawproject/juriscraper)**
  - **Purpose:** A Python scraping library that harvests judicial opinions, oral arguments, and PACER data from American court websites. Serves as the data-gathering layer that feeds CourtListener.
  - **Created:** ~2012
  - **License:** BSD 2-Clause

- **[freelawproject/recap-chrome](https://github.com/freelawproject/recap-chrome)**
  - **Purpose:** The RECAP browser extension for Chrome, Firefox, Safari, and Edge. Allows PACER users to automatically upload documents to the free RECAP Archive while browsing, crowdsourcing public access to federal court records.
  - **Created:** ~2012
  - **License:** GNU General Public License v3 (GPL-3.0)

- **[freelawproject/courts-db](https://github.com/freelawproject/courts-db)**
  - **Purpose:** An open database of over 700 U.S. courts with regex patterns, identifiers, and metadata. Used internally by CourtListener and Juriscraper to normalize court names across sources.
  - **Created:** ~2018
  - **License:** BSD 2-Clause

- **[freelawproject/doctor](https://github.com/freelawproject/doctor)**
  - **Purpose:** A microservice for document and audio file conversion, OCR (using Tesseract), and MP3 processing. Used by CourtListener to extract text from the millions of legal documents in the archive.
  - **Created:** ~2020
  - **License:** BSD 2-Clause

---

## Issue Tracking

- **[CourtListener Issue Tracker](https://github.com/freelawproject/courtlistener/issues)**
  - **Volume:** ~853 open issues (as of early March 2026)
  - **Currency:**
    - Last Day: ~1–3
    - Last Week: ~5–10
    - Last Month: ~20–30
    - Last 6 Months: ~100–150
  - **Activity:**
    - Last Day: ~3–5
    - Last Week: ~15–25
    - Last Month: ~60–80
    - Last 6 Months: ~250+
  - **Beginner Issues:**
    - **Labels:** `help wanted`, `easy pickins` (a project-specific label for approachable issues), `needs-help`
    - **Currency:**
      - Last Week: ~0–1
      - Last Month: ~1–3
      - Last 6 Months: ~10–15
    - **Resolution:**
      - Last Week: ~0–1
      - Last Month: ~1–3
      - Last 6 Months: ~5–10
    - **Approachability:** The `easy pickins` label (seen on issues like #273, #848) tends to mark tasks that are well-scoped Python or Django tasks, often with clear descriptions of what needs to change and why. Issue #848 (SSL verification in PACER scrapers), for example, has a detailed write-up of the problem and multiple possible solutions discussed in comments — the kind of issue a developer could dig into with a few hours of orientation. Comments are constructive and technical. One note: some `help wanted` issues are very old (2014–2017) and may no longer be relevant, so filtering by creation date is important. Newer ones tend to involve data quality or Django feature work.
    - **Summary:** There are a modest number of beginner-friendly issues, and they're generally well-written with enough context to get started. The `easy pickins` label is the most directly newcomer-targeted. The community is responsive on active issues, and maintainers are helpful when contributors show initiative. The biggest caution is that some labeled issues are years old and may be stale — always check recency.

---

## Pull/Merge Requests

- **Volume:** ~101 open PRs (as of early March 2026, per observed data showing 84–101 across recent snapshots)
- **Currency:**
  - Last Week: ~3–5
  - Last Month: ~15–20
  - Last 6 Months: ~60–80
- **Activity:**
  - Last Week: ~5–10
  - Last Month: ~20–30
  - Last 6 Months: ~100+
- **Resolution:**
  - Last Week: ~3–5 merged
  - Last Month: ~15–25 merged
  - Last 6 Months: ~100–150 merged (2,803 closed PRs total as of late 2025)
- **Contributors:**
  - Last Month: ~5–10
  - Last Year: ~20–30
- **New Contributors:**
  - Last Month: ~1–2
  - Last Year: ~8–12
- **Summary:** The project is actively maintained with a steady cadence of PR merges. The CI/CD pipeline (Docker build, CodeQL, Semgrep, lint) runs on every PR. A relatively small, tight-knit group of core contributors drives most activity (maintainers like `mlissner`, `albertisfu`, `ERosendo`, `flooie`, `grossir`), but external contributors do appear and succeed. The PR review process appears thoughtful and technical. A CLA bot handles contributor agreements automatically. PRs from newcomers seem to receive genuine review. The pace is moderate — not overwhelming, but active enough that contributions don't sit unreviewed for long.

---

## Tools/Languages/Libraries/Frameworks

- **Tools:**
  - Docker & Docker Compose — local dev environment orchestration — *used it*
  - GitHub Actions — CI/CD pipelines (lint, test, CodeQL, Semgrep, deploy) — *used it*
  - Sentry — production error monitoring — *heard of it*
  - AWS (S3, Lambda, CloudFormation) — hosting, storage, serverless functions — *used it*
  - Poetry — Python dependency management — *used it*
  - Semgrep — static analysis / security scanning — *heard of it*
  - Tesseract — OCR engine (via Doctor microservice) — *heard of it*

- **Languages:**
  - Python (~62%) — *used it*
  - HTML (~16%) — *expert*
  - JavaScript (~13%) — *used it*
  - PostgreSQL/SQL (~7%) — *used it*
  - CSS (~1%) — *used it*
  - TypeScript (~0.2%) — *used it*

- **Application Libraries/Frameworks:**
  - Django — primary web framework — *used it*
  - Django REST Framework — API layer — *used it*
  - Celery — async task queue — *heard of it*
  - Redis — caching, task brokering — *used it*
  - Elasticsearch — full-text search and alerts — *heard of it*
  - HTMX — lightweight server-driven frontend interactions — *heard of it*
  - React — used in select frontend components — *used it*
  - TailwindCSS — utility-first CSS (in adoption) — *used it*

- **Testing Libraries/Frameworks:**
  - Django's built-in test framework (unittest-based) — *used it*
  - pytest (likely, given Python stack) — *used it*
  - Selenium / geckodriver (used in Juriscraper for browser-based scrapers) — *heard of it*

- **Summary:** The technology stack is a very good match for my current skills. Python and Django are the backbone, and I have solid experience with both. PostgreSQL, Redis, Docker, and GitHub Actions are all tools I've worked with before. The newer additions — Celery, Elasticsearch, and HTMX — are things I've heard of but haven't worked with extensively, which makes them exciting learning opportunities rather than intimidating unknowns. The React usage is limited, so not knowing it deeply isn't a barrier. Overall, I'd estimate I'm familiar with ~75% of the stack already and would need to learn the remaining ~25% (primarily Celery, Elasticsearch, and deeper AWS infrastructure), which is achievable.

---

## Assessment

CourtListener is an exceptionally well-aligned project for me as a contributor. The mission — making the legal system more transparent and equitable — directly connects to my interest in government transparency and public policy. The technology stack is a strong match: it's primarily Python/Django, and I'm comfortable with most of the tooling.

**What makes this project approachable:**
The developer wiki is genuinely useful, well-maintained (updated Feb 2026), and covers everything from architecture to CI/CD. The README and volunteer page make it clear how to get started. The maintainers are active, and the `easy pickins` and `help wanted` labels provide concrete entry points. The project's culture, while small, appears professional and collaborative. The Docker-based dev setup means I don't have to fight a complicated local environment.

**What might make contributions harder:**
The Slack workspace is the real hub of communication, and it's not publicly accessible — a newcomer has to get an invitation. GitHub Discussions, the public alternative, is lightly used and often goes unanswered. The stack also involves some components I'm less familiar with (Elasticsearch, Celery, AWS at scale), and the codebase is large and mature, so there's a meaningful ramp-up period before I'd feel productive. The lack of a formal code of conduct is a minor concern, though the community tone appears fine in practice.

**Overall:** I'm genuinely interested in this project. The combination of meaningful mission, familiar tech stack, active maintainers, and clear newcomer pathways makes it one of the stronger candidates I've reviewed. My main concern is the relatively small contributor base — it means the project is healthy and manageable, but it also means there are fewer people to answer questions or review PRs quickly. Still, the maintainers appear attentive, and contributions seem to receive real engagement.