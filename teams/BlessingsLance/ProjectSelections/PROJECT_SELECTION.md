# Projects Considered
- [CourtListener](teams/BlessingsLance/ProjectReviews/CourtListener.md)
- [Scribe](teams/BlessingsLance/ProjectReviews/Scribe.md)
- [Zulip](teams/BlessingsLance/ProjectReviews/Zulip.md)
- ~~[Signal](teams/BlessingsLance/ProjectReviews/Signal.md)~~
- ~~[The Odin Project](teams/BlessingsLance/ProjectReviews/TheOdinProject.md)~~

# Project Install Spikes
- [Scribe](teams/BlessingsLance/ProjectSelections/Scribe.md)
- [Zulip](teams/BlessingsLance/ProjectSelections/Zulip.md)
- CourtListener (deployed website, no installation)

# Project Ranking

| Project Name | Community | Complexity | Activity | Approachability | Appeal |
|---|---|---|---|---|---|
| Scribe | | | | | |
| Zulip | | | | | |
| CourtListener | | | | | |

## Rationale

**Community:** Scribe has the strongest community for newcomers despite being the smallest. Its Matrix chat is public and requires no invite, maintainer `andrewtavis` responds within hours and is explicitly encouraging, there is a published Code of Conduct (the only project of the three with one), and bi-weekly developer syncs give contributors direct face time with the core team. Zulip has a large and active community but requires creating an account to view the main chat, making it harder to evaluate before committing. CourtListener ranks lowest here: its main communication hub is an invite-only Slack workspace, GitHub Discussions are often unanswered (some questions from late 2025 received no response), and there is no published Code of Conduct.

**Complexity:** Scribe is the simplest of the three. The codebase is written entirely in Kotlin with no external services, no Docker, and no backend — language data is bundled as static JSON. The only non-trivial domain-specific concept is the Android `InputMethodService` API. CourtListener is substantially more complex: it is a mature Django web application backed by PostgreSQL, Redis, Celery, and Elasticsearch, all orchestrated with Docker Compose, plus AWS dependencies for certain features. Zulip is the most complex overall — the codebase spans Python (57%), TypeScript (18%), JavaScript (9%), and more, uses Django, Tornado, and Webpack together, and has over 1,200 open issues reflecting the scope of active work. Both CourtListener and Zulip require meaningful ramp-up time before a contributor can feel productive; Scribe does not.

**Activity:** Zulip is the most active project by a wide margin — multiple new issues and PRs per week, a large and engaged contributor base, and an upcoming release actively under development. CourtListener is consistently active at a moderate pace: 20–30 new issues per month, 15–20 PRs per month, and a small core team of 5–10 maintainers who review contributions promptly. Scribe has the lowest raw activity — roughly 2–5 new issues and 1–3 PRs per month — but this is appropriate for its size, and a steady stream of Weblate translation PRs keeps the repository visibly alive. For all three, the pace of activity is sustainable; none are stale or moving too fast to follow.

**Approachability:** Scribe is the most approachable by a meaningful margin. The CONTRIBUTING.md explicitly welcomes contributors new to Kotlin, the install spike required only Android Studio and a few setup steps (no Docker, no virtual machine), `good first issue` labels are fresh (batch opened February 2025), and issues are well-scoped with design references and code pointers. CourtListener is moderately approachable — the developer wiki is thorough and recently updated, `easy pickins` issues provide concrete entry points, but the Docker-based multi-service setup adds friction and the closed Slack workspace means a newcomer's first questions may go unanswered publicly. Zulip is the least approachable: setup requires Vagrant or WSL with several hundred megabytes of dependencies, the project has its own Git workflow that even experienced Git users must learn, and the large codebase and polyglot stack mean a longer orientation period before productive contribution.

**Appeal:** <!-- Fill in based on your team's discussion — which project domain, technologies, and goals resonate most with both team members. Consider: Scribe's privacy-first language learning keyboard (100% Kotlin/Android), Zulip's distributed team chat platform (Python/TypeScript/Django), and CourtListener's legal transparency platform (Python/Django). Which project would you be most motivated to work on throughout the semester? -->

# Project Selection

**Project:** <!-- Name of the selected project -->

**Rationale:** <!-- A paragraph explaining the team's reasoning. Describe how the rankings were considered, which dimensions were weighted most heavily and why. -->

**Install Estimate:** <!-- Rough estimate of how many hours it will take all team members to get the development environment up and running. -->

**Knowledge Gaps:**
- <!-- Tool/language/framework that needs to be learned, and brief explanation -->

**Concerns:**
- <!-- Any remaining concerns about working on the selected project, with brief explanation -->