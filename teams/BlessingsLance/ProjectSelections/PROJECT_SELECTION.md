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
| Scribe | 1 | 1 | 3 | 1 | 1 |
| Zulip | 2 | 3 | 1 | 3 | 2 |
| CourtListener | 3 | 2 | 2 | 2 | 3 |
## Rationale

**Community:** Scribe has the strongest community for newcomers despite being the smallest. Its Matrix chat is public and requires no invite, maintainer `andrewtavis` responds within hours and is explicitly encouraging, there is a published Code of Conduct (the only project of the three with one), and bi-weekly developer syncs give contributors direct face time with the core team. Zulip has a large and active community but requires creating an account to view the main chat, making it harder to evaluate before committing. CourtListener ranks lowest here: its main communication hub is an invite-only Slack workspace, GitHub Discussions are often unanswered (some questions from late 2025 received no response), and there is no published Code of Conduct.

**Complexity:** Scribe is the simplest of the three. The codebase is written entirely in Kotlin with no external services, no Docker, and no backend — language data is bundled as static JSON. The only non-trivial domain-specific concept is the Android `InputMethodService` API. CourtListener is substantially more complex: it is a mature Django web application backed by PostgreSQL, Redis, Celery, and Elasticsearch, all orchestrated with Docker Compose, plus AWS dependencies for certain features. Zulip is the most complex overall — the codebase spans Python (57%), TypeScript (18%), JavaScript (9%), and more, uses Django, Tornado, and Webpack together, and has over 1,200 open issues reflecting the scope of active work. Both CourtListener and Zulip require meaningful ramp-up time before a contributor can feel productive; Scribe does not.

**Activity:** Zulip is the most active project by a wide margin — multiple new issues and PRs per week, a large and engaged contributor base, and an upcoming release actively under development. CourtListener is consistently active at a moderate pace: 20–30 new issues per month, 15–20 PRs per month, and a small core team of 5–10 maintainers who review contributions promptly. Scribe has the lowest raw activity — roughly 2–5 new issues and 1–3 PRs per month — but this is appropriate for its size, and a steady stream of Weblate translation PRs keeps the repository visibly alive. For all three, the pace of activity is sustainable; none are stale or moving too fast to follow.

**Approachability:** Scribe is the most approachable by a meaningful margin. The CONTRIBUTING.md explicitly welcomes contributors new to Kotlin, the install spike required only Android Studio and a few setup steps (no Docker, no virtual machine), `good first issue` labels are fresh (batch opened February 2025), and issues are well-scoped with design references and code pointers. CourtListener is moderately approachable — the developer wiki is thorough and recently updated, `easy pickins` issues provide concrete entry points, but the Docker-based multi-service setup adds friction and the closed Slack workspace means a newcomer's first questions may go unanswered publicly. Zulip is the least approachable: setup requires Vagrant or WSL with several hundred megabytes of dependencies, the project has its own Git workflow that even experienced Git users must learn, and the large codebase and polyglot stack mean a longer orientation period before productive contribution.

**Appeal:** We both are interested in Android development, so both Zulip and Scribe are appealing. The web-based aspect of CourtListener is less of a draw because of this. The installation procedure also took a little longer and was more involved with Zulip, making it less of an appeal to the simpler and easier to navigate process of Scribe installation and environment setup. The stacks involved in CourtListener and Zulip also present technical challenges that would be steep learning curves not present with Scribe.

# Project Selection

**Project:** Scribe

**Rationale:** Our team selected Scribe as our open source project primarily because of its Android development focus, which aligns well with our interests and growth goals. The community surrounding Scribe is welcoming and easily accessible, making it a strong fit for contributors looking to engage meaningfully without a steep onboarding curve. The issues available in the repository are clearly defined and straightforward, allowing us to contribute effectively within a realistic timeframe. Additionally, Scribe presents an exciting opportunity to work with Kotlin, a language we're eager to gain hands-on experience with, while also leveraging our existing familiarity with Python where applicable. The combination of a supportive community, well-scoped tasks, and the chance to expand our technical skill set made Scribe a clear choice for our team.

**Install Estimate:** 30 - 40 mins

**Knowledge Gaps:**

***Blessings***
- **Kotlin:** I do not have prior experience writing Kotlin, which is the primary language used throughout the Scribe-Android codebase. Learning Kotlin's syntax, conventions, and Android-specific idioms will be an early priority.
- **Jetpack Compose:** The project is actively migrating its UI from legacy Fragments and XML layouts to Jetpack Compose, Android's modern declarative UI framework. We will need to learn Compose's component model and state management to contribute to both new and migrated UI code.
- **InputMethodService (IME):** Scribe-Android is fundamentally a custom keyboard app built on Android's InputMethodService API. Understanding how IMEs handle text input, key events, and interaction with other apps is essential and represents a significant learning curve for us.
- **Gradle:** While I have basic familiarity with Android Studio, I have limited hands-on experience configuring Gradle build files, managing dependencies, and working with build variants — the project uses two variants (keyboard and conjugate) that we'll need to understand.
- **Figma:** Scribe's designs are maintained in a public Figma file, and design contributions are encouraged. We have very limited experience with Figma and will need to become comfortable navigating and potentially contributing to design files.
- **Android Development (general):** I only have foundational knowledge of Android development, so ramping up on core concepts like Activities, Services, and the Android lifecycle will be necessary alongside the more specialized topics above.

***Lance***
- **Input Method Service (IME)**: Scribe uses this to handle text input and key events. I am not familiar with this, and will have to learn more about it.
- **MockK**: Kotlin-native mocking library. I've used it a little bit, but not enough to feel confident saying there isn't some knowledge gap here.
- **Android Instrumented Tests**: For testing some of the app's functionality. Similar to MockK, I've used this a bit but there is still a gap here.

- **Figma**: I've heard of Figma, but never used it. This will be a gap I will have to learn.

**Concerns:**

The primary concern is the steep initial learning curve of contributing to a custom keyboard application. Building an IME is a fairly niche area of Android development, and most beginner-friendly Android tutorials and resources do not cover InputMethodService in depth, which may make self-guided learning more challenging. Additionally, since the project is actively migrating from legacy Android Views to Jetpack Compose, the codebase is in a transitional state where both paradigms coexist — this could be confusing as newcomers trying to understand established patterns and conventions. We are also mindful that the project's language data pipeline depends on Wikidata and SPARQL queries managed through the separate Scribe-Data repository, meaning that debugging data-related issues may require us to work across multiple repos and tech stacks simultaneously. Finally, while the project is very welcoming to newcomers and labels issues with "good first issue," much of the open work tagged as high priority involves deeper architectural changes, so finding contributions that match our current skill level while still being meaningful may take some effort early on. That said, the active Matrix chat community and bi-weekly developer syncs should help us get oriented and unblocked when needed.
