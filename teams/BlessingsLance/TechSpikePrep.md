# Tech Spike Preparation

**Project:** [Scribe-Android](https://github.com/scribe-org/Scribe-Android)

**Team:** Blessings and Lance

---

## Gap Analysis

### Our Current Situation

#### Lance

**Knowledge & Skills:**
- **Languages:** Kotlin, Python, Shell, JavaScript, SQL
- **Android:** Android Studio, Gradle (Kotlin DSL), ADB/Android Emulator, Android Jetpack (ViewModel, LiveData, Navigation, ViewPager2), Jetpack Compose, SharedPreferences
- **Tools:** GitHub Actions (CI), pre-commit/ktlint, Hugging Face Transformers
- **Testing:** JUnit (heard of), MockK (limited hands-on), Android Instrumented Tests (limited hands-on)
- **Other:** Git, Python scripting

**Strengths:** Familiarity with the Android development ecosystem, Kotlin, and modern Jetpack libraries. Comfortable with CI tooling and pre-commit workflows. Prior experience with Jetpack Compose gives a solid foundation for the active UI migration in Scribe.

**Weaknesses/Gaps:** No hands-on experience with `InputMethodService` (the Android keyboard API central to Scribe). Limited testing experience with MockK and Android Instrumented Tests. Heard of Figma but never used it.

**Interests:** Android UI development, Jetpack Compose, testing infrastructure.

---

#### Blessings

**Knowledge & Skills:**
- **Languages:** Python, JavaScript, HTML/CSS
- **Android:** Android Studio (basic), Gradle (basic familiarity)
- **Tools:** GitHub Actions (CI), pre-commit
- **Other:** Git

**Strengths:** Python experience (relevant to Scribe-Data pipeline), general software development background, strong organizational and communication skills.

**Weaknesses/Gaps:** No prior Kotlin experience. Limited Android development knowledge (Activities, Services, Android lifecycle). No experience with Jetpack Compose. No hands-on experience with `InputMethodService`. Limited Gradle configuration experience. No experience with Figma.

**Interests:** Mobile development, open source contribution, learning Kotlin.

---

### Our Goals

The following technologies, languages, and frameworks are required to contribute effectively to Scribe-Android, listed in order of priority:

| Priority | Technology | Why It Matters |
|---|---|---|
| 1 | **Kotlin** | 100% of the Scribe-Android codebase. All contributions require it. |
| 2 | **InputMethodService (IME API)** | The core Android API that powers Scribe's custom keyboard. Understanding it is prerequisite to most feature work. |
| 3 | **Jetpack Compose** | The project is actively migrating from Fragments/XML to Compose (Issue #150). New UI contributions must use Compose. |
| 4 | **Android Jetpack** (ViewModel, LiveData, Navigation) | Used throughout the app for state and navigation. |
| 5 | **Gradle** | Required to manage dependencies, configure build variants (`keyboardDebug` / `conjugateDebug`), and run tasks. |
| 6 | **JUnit / MockK / Android Instrumented Tests** | Testing is expected for contributions; MockK is the Kotlin-native mock library referenced in the project (Issue #197). |
| 7 | **Figma** | UI designs are maintained in a public Figma file; relevant for design-facing contributions. |
| 8 | **pre-commit / ktlint / detekt** | All commits must pass automated linting; contributors must understand what the hooks enforce. |
| 9 | **SPARQL / Scribe-Data** | Relevant only for data pipeline contributions; lower priority for initial Android UI work. |

**Sources consulted:** [CONTRIBUTING.md](https://github.com/scribe-org/Scribe-Android/blob/main/CONTRIBUTING.md), [ARCHITECTURE.md](https://github.com/scribe-org/Organization/blob/main/ARCHITECTURE.md), project issue tracker, Scribe-Android tools/languages section from team's project review.

---

### Our Gaps

#### Team Gaps (no one has this skill)

- **InputMethodService (IME API)** — Neither team member has worked with Android's keyboard extension framework. This is the highest-priority team gap, as it underpins all of Scribe's core functionality.
- **Figma** — Neither team member has used Figma. Lower priority, but needed for design-facing issues.

#### Individual Gaps

| Gap | Blessings | Lance |
|---|---|---|
| Kotlin | No prior experience | Comfortable |
| Jetpack Compose | No experience | Familiar |
| Android development (general) | Foundational | Comfortable |
| Gradle configuration | Limited | Comfortable |
| MockK | No experience | Limited hands-on |
| Android Instrumented Tests | No experience | Limited hands-on |
| IME API | No experience | No experience |
| Figma | No experience | No experience |

---

### Our Plan

Given the time available for the Tech Spike, we will focus on the highest-priority gaps first. The goal is to reach a level where each team member can contribute to a well-scoped `good first issue`.

| Gap | Who | Rationale |
|---|---|---|
| **Kotlin fundamentals** | Both | Blessings needs foundational Kotlin; Lance can help unblock. |
| **InputMethodService (IME API)** | Both | Highest-priority team gap; both must understand it to work on any keyboard feature. |
| **Jetpack Compose** | Blessings (primary) | Lance is already familiar; Blessings needs exposure. Active migration (Issue #150) is the most accessible entry point. |
| **MockK / Android Instrumented Tests** | Lance (primary) | Lance has interest in testing infrastructure; MockK is referenced in open issues. |
| **Figma** | Both (low priority) | Only needed for design contributions; will address if time allows. |
| **Gradle** | Both | We can focus on understanding build variants and dependency management. |

---

## Learning Resources

### Kotlin

> **W3Schools (https://www.w3schools.com/kotlin/index.php)**
W3Schools offers an excellent starting point for anyone new to Kotlin, breaking down the language's core concepts and code structure in a clear, beginner-friendly format. Its step-by-step approach makes it easy to build foundational knowledge without feeling overwhelmed, which is especially valuable for developers transitioning from other languages. As a free and widely trusted resource, it serves as a reliable first stop before diving into more advanced documentation or project-specific code.

> **Kotlin Official Documentation (kotlinlang.org)**
The official Kotlin documentation is an essential resource for any developer working with the language. It offers comprehensive coverage of everything from basic syntax to advanced features like coroutines and multiplatform development. What makes it particularly useful is that it's maintained directly by JetBrains, the creators of Kotlin, so it's always up to date and authoritative. It also includes hands-on examples and a built-in playground for experimenting with code directly in the browser.

### InputMethodService (IME API)

> TODO: Find 2–4 resources. We can start with the [Android IME developer guide](https://developer.android.com/develop/ui/views/touch-and-input/creating-input-method). Ask the Scribe Matrix community for any IME-specific resources they recommend.

### Jetpack Compose

> TODO: Find 2–4 resources. We can start with official Jetpack Compose pathway on developer.android.com, "Compose Camp" codelabs.

### MockK / Android Testing

> TODO: Find 2–4 resources. We can start with the [MockK docs](https://mockk.io/) and Android's testing guides. Check Issue #197 in Scribe-Android for context on expected test patterns.

### Figma (low priority)

> TODO: Find a couple resources.

---

## Planned Spike Artifacts

- **Blessings & Lance** — A minimal Android app implementing a custom `InputMethodService` keyboard from scratch, following an IME tutorial. *External to Scribe project. From learning resource.*

- **Blessings** — A simple screen built entirely in Jetpack Compose (e.g., a settings-style UI) demonstrating state management with `ViewModel` and `StateFlow`. *External to Scribe project. From learning resource.*

- **Lance** — A MockK-based unit test suite for an existing Scribe-Android class (e.g., a `ViewModel` or utility function), following the patterns referenced in Issue #197. *Internal to Scribe project. Team-designed.*
