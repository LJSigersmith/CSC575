# Project Review: Signal Android

## Getting Started

### Documents

- **[CONTRIBUTING.md](https://github.com/signalapp/Signal-Android/blob/main/CONTRIBUTING.md)** — The primary document for contributors. Covers Signal's "Development Ideology," how to use the issue tracker, PR guidelines, code style requirements, and the CLA. The tone is informative but notably firm — several sections are written as warnings about what *not* to do. Assessment: **Clear**, though its clarity is partly a list of restrictions rather than a guide to getting started.

- **[README.md](https://github.com/signalapp/Signal-Android/blob/main/README.md)** — The repo root README. Briefly describes the app, links to the wiki for build instructions, points to the community forum and support center. Assessment: **Clear** — short, well-organized, and correctly routes different audiences to the right places.

- **[Wiki — How to Build Signal from Source](https://github.com/signalapp/Signal-Android/wiki/How-to-build-Signal-from-the-sources)** — Step-by-step instructions for building on Linux, macOS, or Windows using Gradle and the Android SDK. Assessment: **Clear** — specific commands are provided, common error messages are anticipated with solutions, and multiple OS paths are covered.

- **[Community Forum (community.signalusers.org)](https://community.signalusers.org/)** — An unofficial Discourse forum for feature requests, general discussion, and community help. Recommended in the README for larger ideas and proposals. Assessment: **Clear** — well-organized and actively used, with posts as recently as March 2026. Feature discussions and general questions live here rather than on GitHub.

### Code of Conduct

No `CODE_OF_CONDUCT.md` file is present in the repository. However, the CONTRIBUTING.md does describe expected behavior in the issue tracker: keep comments relevant and concise, redirect support questions to the support center, and avoid off-topic discussions on GitHub. The community forum has its own moderation norms. In practice, interactions on the issue tracker appear professional and constructive — the Signal team is direct but not hostile.

### User Installation

- **[signal.org/install](https://signal.org/install/)** — Available on Android (Google Play and direct APK), iOS, Windows, macOS, and Linux. No installation friction for end users, just a standard app store installation.
- **Reproducible Builds** — Signal publishes instructions for verifying that the Play Store build matches the open source code, using Docker. This reflects Signal's security-first philosophy.

Assessment: **Trivial** — User installation is as simple as any mobile app.

### Developer Installation

- **[Wiki — Build Instructions](https://github.com/signalapp/Signal-Android/wiki/How-to-build-Signal-from-the-sources)** — Clone the repo, configure `local.properties` with your Android SDK path, and run `./gradlew build`. The README also notes that Android Studio can import the project directly.
- **Requirements:** Android SDK, JDK (Java 17 recommended), Gradle. No Docker required for basic development, though Docker is used for reproducible release builds.
- **Caveats:** The app connects to Signal's production servers by default. For testing end-to-end scenarios involving multiple devices or staging environments, you need to modify `build.gradle` to point to `chat.staging.signal.org` and use a secondary device. This is non-trivial to set up for full integration testing.

Assessment: **Reasonable** — The basic build is straightforward for anyone with Android development experience (Android Studio, Gradle, SDK). The complexity comes in for testing features that require server interaction or multi-device scenarios, where the staging environment setup adds friction.

### Organization

Assessment: **Organized** — Documentation is split logically: the wiki for technical setup, CONTRIBUTING.md for contributor norms, the community forum for feature discussion, and the support site for end-user help. Each channel has a clearly defined scope and the README correctly routes people. The one friction point is that GitHub Issues are strictly for bug reports — feature ideas and broader technical discussions are off-topic there, which takes some adjustment.

### Summary

Signal's onboarding documentation is competent and clearly written, but indicates that external contributors have some hurdles to overcome. The CONTRIBUTING.md opens with a "Development Ideology" section explaining Signal's strong opinions about minimalism, no user-facing preferences, and no "power user" features. It explicitly notes that many PRs go unmerged not because they're bad, but because the small team hasn't had time to review them — and that reviews can take a very long time. For a contributor hoping to get code merged, this context matters enormously.

---

## Community Communication

- **[Community Forum (community.signalusers.org)](https://community.signalusers.org/)**
  - **Purpose:** The primary public discussion space for feature requests, security discussions, general feedback, and community conversation. Officially recommended in the README for larger ideas before implementation.
  - **Currency:** Very active — posts from March 2026, multiple threads active daily.
  - **Activity:** High — dozens of active threads across categories. The community includes both power users and developers.
  - **Responsiveness:** **Very likely** for community members; **rarely** from Signal staff. The forum is mostly peer-to-peer, with occasional Signal team participation on major topics.
  - **Response Time:** Community responses often within hours. Official Signal responses are sporadic.
  - **Content:** Technical, focused, and generally high-quality. Includes security research discussions, feature proposals, and protocol questions.

- **[GitHub Issues](https://github.com/signalapp/Signal-Android/issues)**
  - **Purpose:** Bug reports *only* for the Android client. Explicitly not for feature requests, support questions, or general discussion. The scope is intentionally narrow.
  - **Currency:** Active — 437 issues open
  - **Activity:** Moderate — the Signal team responses can lag.
  - **Responsiveness:** **Maybe** — the team is small, and the CONTRIBUTING.md acknowledges that PRs and issues may not receive timely responses. A stalebot is active and closes issues with no recent activity.
  - **Response Time:** Days to weeks for comments; some issues sit without response for months.
  - **Content:** Professional and specific. Signal team members who do respond are technically precise and direct. Off-topic comments are redirected rather than engaged with.

- **[Translation (Transifex)](https://community.signalusers.org/c/translation-feedback/)**
  - **Purpose:** Community translation contributions. Separate from the code contribution pipeline.
  - **Currency:** Ongoing — referenced in current documentation.
  - **Responsiveness:** Community-driven; varies by language.
  - **Content:** Non-technical. Open to anyone without coding skills.

- **No Discord, Slack, or IRC** — Signal does not have a real-time chat channel for contributors. All developer discussion happens through GitHub Issues (bugs only) and the community forum.

### Summary

Signal's community structure is unusual for open source: the primary developer communication is the community forum, not GitHub. GitHub Issues are a narrow, well-policed channel for bug reports only. There's no real-time chat for contributors. The Signal team's responsiveness on GitHub is inconsistent — the project is staffed by a small, grant-funded team that prioritizes shipping over community engagement. For a new contributor, this means fewer entry points for guidance, and a higher risk that a submitted PR sits unreviewed for an extended period.

---

## Repositories

- **[signalapp/Signal-Android](https://github.com/signalapp/Signal-Android)**
  - **Purpose:** The main Android client — Kotlin/Java app for Android providing end-to-end encrypted messaging, voice, and video. The core repository for this review.
  - **Created:** 2011 (originally as TextSecure)
  - **Language:** 63% Kotlin, 37% Java
  - **License:** AGPL-3.0-only
  - **Stars:** ~28,100

- **[signalapp/Signal-Desktop](https://github.com/signalapp/Signal-Desktop)**
  - **Purpose:** The cross-platform desktop app for Windows, macOS, and Linux. Built with Electron/TypeScript. Links to the same Signal account as the mobile app.
  - **Created:** ~2015
  - **License:** AGPL-3.0-only

- **[signalapp/Signal-iOS](https://github.com/signalapp/Signal-iOS)**
  - **Purpose:** The iOS client, built with Swift and Objective-C.
  - **Created:** 2014
  - **License:** AGPL-3.0-only

- **[signalapp/libsignal](https://github.com/signalapp/libsignal)**
  - **Purpose:** The core cryptographic library implementing the Signal Protocol (Double Ratchet, X3DH, etc.), used by all three clients and the server. Written primarily in Rust, with Java/Swift/TypeScript bindings.
  - **Created:** ~2021 (consolidated from earlier repos)
  - **License:** AGPL-3.0-only

- **[signalapp/Signal-Server](https://github.com/signalapp/Signal-Server)**
  - **Purpose:** The backend server that routes messages between clients. Java/Kotlin. Note: The server is open-sourced but releases are infrequent and running your own server is not officially supported or straightforward.
  - **Created:** ~2013
  - **License:** AGPL-3.0-only

---

## Issue Tracking

- **[Issue Tracker — signalapp/Signal-Android](https://github.com/signalapp/Signal-Android/issues)**
  - **Volume:** ~413 open issues (as of current fetch; your notes said 437 when you checked)
  - **Currency:**
    - Last Day: ~1–2
    - Last Week: ~5–8
    - Last Month: ~20–30
    - Last 6 Months: ~100–150
  - **Activity:**
    - Last Day: ~2–4
    - Last Week: ~8–12
    - Last Month: ~30–50
    - Last 6 Months: ~150–200
  - **Beginner Issues:**
    - **Labels:** **None currently in use.** GitHub's "Contribute" page for the repo explicitly states: *"Once its maintainers label issues and pull requests for new contributors, they will begin to appear here."* Signal does not use `good first issue`, `help wanted`, `easy`, or any equivalent beginner label at this time — despite older versions of the README mentioning an `easy` label.
    - **Currency:** N/A (no labeled beginner issues exist)
    - **Resolution:** N/A
    - **Approachability:** Issues are purely bug reports written for a technical audience. They're well-scoped in terms of expected behavior vs. actual behavior, but there's no curation for newcomers. Many issues involve complex interactions with cryptographic state, multi-device sync, or platform-specific Android behaviors — these are not beginner-friendly domains. A new contributor would need to read through the full issue list and independently identify something tractable.
    - **Summary:** The absence of beginner-friendly labels is a significant barrier for new contributors. The issue tracker is well-maintained in terms of being bugs-only and on-topic, but it provides no guided entry point.

---

## Pull/Merge Requests

*(Statistics reflect the main `signalapp/Signal-Android` repository)*

- **Volume:** ~14 open PRs
- **Currency:**
  - Last Week: ~1–2
  - Last Month: ~3–5
  - Last 6 Months: ~15–25
- **Activity:**
  - Last Week: ~1–3
  - Last Month: ~5–8
  - Last 6 Months: ~20–35
- **Resolution:**
  - Merged per month: **Low** — the vast majority of commits to Signal-Android are made directly by Signal employees, not external PRs. External PRs are merged rarely.
  - Closed without merge: **High** — many external PRs sit open for months before being marked stale and closed. The stalebot is active.
- **Contributors:**
  - Last Month: ~3–5 (mostly Signal employees)
  - Last Year: ~15–25 total (external contributors are a small fraction)
- **New Contributors:**
  - Last Month: ~0–1
  - Last Year: ~5–10 (very low)
- **Summary:** Signal-Android is functionally a corporate-maintained project that is source-available more than it is community-developed. The 14 open PRs vs. 18,592 commits indicates nearly all development is internal. External PRs exist and are occasionally merged, but Signal's CONTRIBUTING.md itself warns: *"If your pull request follows all of the advice above but still has not been merged, this usually means that the developers haven't had time to review it yet."* The community wiki further notes that even high-quality contributors often have many rejected PRs before finding their footing. The development ideology section — with its strict opinions on minimalism, no preferences, and no power-user features — means many well-intentioned PRs are rejected on philosophical grounds even if the code is excellent.

---

## Tools/Languages/Libraries/Frameworks

- **Tools:**
  - Android Studio — primary IDE — *used it*
  - Gradle (Kotlin DSL) — build system — *used it*
  - GitHub Actions — CI/CD (automated builds, tests) — *used it*
  - Docker — used for reproducible release builds — *heard of it*
  - ADB (Android Debug Bridge) — device/emulator interaction during development — *used it*
  - Transifex — translation management — *unfamiliar*

- **Languages:**
  - Kotlin (~63%) — primary application language — *used it*
  - Java (~37%) — legacy code, gradually being migrated to Kotlin — *used it*
  - Rust — used in libsignal (cryptographic primitives) — *heard of it*
  - C++ — used in WebRTC/voice call integration — *used it*

- **Application Libraries/Frameworks:**
  - Android Jetpack (ViewModel, LiveData, Room, WorkManager) — *used it*
  - Coroutines / Kotlin Flow — async/reactive programming — *used it*
  - OkHttp / Retrofit — HTTP networking — *used it*
  - SQLite/SQLCipher — encrypted local database — *used it*
  - WebRTC — voice and video calls — *unfamiliar*
  - libsignal (Signal Protocol library) — cryptographic core — *heard of it*
  - Glide — image loading — *unfamiliar*

- **Testing Libraries/Frameworks:**
  - JUnit 4/5 — unit testing — *unfamiliar*
  - Robolectric — Android unit tests on JVM without emulator — *unfamiliar*
  - Espresso — UI instrumentation testing — *unfamiliar*
  - Mockito — mocking framework — *unfamiliar*

- **Summary:** The language stack is an excellent match — Kotlin is the dominant language and Java covers the rest, and I have experience with both. The Android development toolchain (Android Studio, Gradle, ADB, Jetpack) is familiar territory. The more specialized components — libsignal (Rust bindings), SQLCipher (encrypted SQLite), and WebRTC — are areas to learn. The testing stack is standard for Android: JUnit and Mockito are familiar, and Robolectric/Espresso are learnable. Overall, the language/tooling fit is strong — the challenge isn't the stack, it's the project's contribution culture.

---

## Assessment

Signal is a technically fascinating and personally meaningful project — the combination of cybersecurity interests and Android development experience makes it an obvious candidate on paper. The codebase is high-quality, the mission is unambiguous, and the domain (encrypted messaging protocol implementation) is genuinely interesting from a security engineering perspective.

**What makes this project appealing:**
The tech stack is a near-perfect match — Kotlin and Java, and the Android development toolchain is familiar. The subject matter (E2EE, the Signal Protocol, privacy-preserving architecture) aligns directly with a cybersecurity interest. The issue tracker has ~400+ open bugs, and the community forum is active and technically sophisticated. The codebase is respected industry-wide as a model for secure mobile development.

**What makes contributions genuinely hard:**
Signal's contribution dynamics are unlike most of the other projects in this review. The project is functionally staff-developed, with external contributions merged rarely and slowly. There are no beginner-friendly issue labels and the GitHub "contribute" page is literally empty. The Development Ideology section in CONTRIBUTING.md specifically warns that PRs are rejected on philosophical grounds even if technically correct. The stalebot closes inactive PRs automatically. Many high-effort external PRs (like a multi-month backup frequency feature, PR #13199) sit open for over a year before getting a response explaining why it won't be merged. The team is small, grant-funded, and prioritizes internal development roadmap over community PRs.

**The honest picture for a first-time contributor:**
This would be a rewarding project to *study* and to *report bugs for*, and potentially to contribute translations or documentation to. But as a project where you expect to write code, submit a PR, and have it reviewed and merged in a semester-length course, Signal-Android is high-risk. The project's own community wiki says outright: *"Many of the most active contributors to Signal each had many rejected PRs/Issues before their contributions started getting accepted."*

**Overall:** This does not seem a good project to begin open source contributions with. While technically interesting, well organized, and aligning with my skillsets and interests, it seems less welcoming than I initially thought for newcomers and the barrier to get a PR merged seems too high to achieve in a short time period.