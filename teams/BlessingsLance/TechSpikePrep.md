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

> **Kotlin Official Documentation (https://kotlinlang.org/)**
The official Kotlin documentation is an essential resource for any developer working with the language. It offers comprehensive coverage of everything from basic syntax to advanced features like coroutines and multiplatform development. What makes it particularly useful is that it's maintained directly by JetBrains, the creators of Kotlin, so it's always up to date and authoritative. It also includes hands-on examples and a built-in playground for experimenting with code directly in the browser.

> **Android Developers – Kotlin for Android (https://developer.android.com/kotlin)** 
Android Developers is Google's official learning pathway tailored specifically to mobile development. This resource is particularly relevant for our work on Scribe, as it connects Kotlin fundamentals directly to Android app architecture, UI design, and best practices. It includes codelabs, sample projects, and integration guides that bridge the gap between learning Kotlin in isolation and applying it within a real Android codebase.

### InputMethodService (IME API)

> **Android Input Method Editor (IME) Developer Guide (https://developer.android.com/develop/ui/views/touch-and-input/creating-input-method)**
IME Developer Guide is an essential starting point for understanding how custom keyboards are built on Android. It walks through the full lifecycle of an IME, covering how to declare the input method service, design the keyboard UI, handle text input and composing, and manage different input types. Since Scribe functions as a custom keyboard, understanding this guide is foundational to contributing meaningfully to the project.

> **Android InputMethodService API Reference (https://developer.android.com/reference/android/inputmethodservice/InputMethodService)**
This resource complements the IME guide by providing the detailed technical reference for the core class that powers any custom keyboard. It documents every method and callback available for managing input connections, handling key events, and controlling the candidate view. This is the resource to consult when working directly with Scribe's keyboard service code and needing to understand specific behaviors or override points.

> **Scribe Community – Matrix Chat (https://matrix.to/#/#scribe_community:matrix.org)** 
This is the project's primary communication channel where contributors and maintainers discuss development, answer questions, and share resources. Reaching out here for IME-specific resources, tips, or guidance from experienced contributors would be a valuable next step. The community has been noted for its accessibility and willingness to help newcomers get oriented.


### Jetpack Compose

> **Jetpack Compose for Android (https://developer.android.com/develop/ui/compose)** 
This is Google's official pathway for learning Compose, the declarative UI framework that is quickly becoming the standard for Android development. It covers core concepts like composable functions, state management, layouts, theming, and animation. Since Scribe's Android app relies on modern UI practices, understanding Compose is important for contributing to any front-facing components of the project.

> **Compose Camp Codelabs (https://developer.android.com/courses/android-basics-compose/course)**
Compose Camp Codelabs is a hands-on, self-paced learning series offered through Google's Android Basics with Compose course. It guides learners through building real Android apps using Compose from the ground up, with interactive codelabs that reinforce each concept through practice. This is particularly useful for developers who are new to declarative UI patterns and want a structured path rather than jumping straight into documentation.

> **Jetpack Compose Samples (https://github.com/android/compose-samples)**
This is a GitHub repository maintained by Google containing a collection of real-world sample apps built entirely with Compose. Exploring these projects offers practical insight into how Compose is used in production-style codebases, including navigation, state handling, and API integration. Studying these samples can help bridge the gap between tutorial exercises and contributing to a live project like Scribe.


### MockK / Android Testing

> **MockK Documentation (https://mockk.io/)**
The official reference for MockK, a mocking library built specifically for Kotlin. It supports Kotlin-specific features like coroutines, extension function mocking, and object mocks MockK, making it far more natural to use in a Kotlin project than Java-based alternatives like Mockito. Scribe-Android already supports unit testing with JUnit and mocking with MockK GitHub, so understanding this library is essential for contributing test code to the project. The docs cover everything from basic stubbing and verification to advanced techniques like relaxed mocks and spy objects.

> **Android Testing Fundamentals (https://developer.android.com/training/testing/fundamentals)** 
This is Google's official guide to testing Android applications. It covers the core tenets of testing Android apps, distinguishing between local tests that run on a development machine and instrumented tests that run on a device Android Developers. The guide also walks through testable architecture patterns, including how to decouple code for easier testing — a concept directly relevant to Scribe, where contributors may need to refactor components to make them mockable.

>**Android Local Unit Tests Guide (https://developer.android.com/training/testing/local-tests)**
Android local unit testing guide dives deeper into writing unit tests that run on the host machine without an Android device. It covers how to replace dependencies using test doubles like fakes or mocks, and discusses considerations around the mockable Android library Android Developers. This resource is particularly relevant since Scribe-Android's testing needs center on local unit tests with MockK, and understanding how to handle Android framework dependencies in isolation is key to writing effective tests for the project.

### Figma (low priority)

> **Figma Design for Beginners (https://help.figma.com/hc/en-us/sections/30880632542743-Figma-Design-for-beginners)**
Figma's own official beginner course, featuring expert-led video tutorials. The hands-on course walks through designing a portfolio website from scratch, covering the basics like shapes, text, and frames, and progressing into more advanced features like auto layout, components, and prototyping Figma Help Center. This is the most reliable starting point since it comes directly from Figma and stays in sync with the latest interface updates. It's especially useful for contributors who need to review or reference Scribe's public designs on Figma.

> **Designlab – Figma 101 (https://designlab.com/figma-101-course/introduction-to-figma)**
Designlab is a free seven-day email course that guides you through building your own app design and prototype in Figma. It introduces all of the key functions in Figma by having you build a set of app screens, then uses Figma's prototyping functionality to link them together Designlab. The structured daily format makes it easy to fit into a busy schedule, and the project-based approach means you walk away with a tangible portfolio piece rather than just theoretical knowledge.

> **Figma Resource Library – Design Basics (https://www.figma.com/resource-library/design-basics/)**
This is a collection of articles and guides hosted by Figma that covers foundational design principles including UI versus UX, typography, color theory, and prototyping. Rather than a single linear course, it serves as a reference library you can dip into based on what you need at any given moment. This is valuable for contributors who may be comfortable with the tool itself but want to strengthen their understanding of the design thinking behind Scribe's interface decisions.
---

## Planned Spike Artifacts

- **Blessings & Lance** — A minimal Android app implementing a custom `InputMethodService` keyboard from scratch, following an IME tutorial. *External to Scribe project. From learning resource.*

- **Blessings** — A simple screen built entirely in Jetpack Compose (e.g., a settings-style UI) demonstrating state management with `ViewModel` and `StateFlow`. *External to Scribe project. From learning resource.*

- **Lance** — A MockK-based unit test suite for an existing Scribe-Android class (e.g., a `ViewModel` or utility function), following the patterns referenced in Issue #197. *Internal to Scribe project. Team-designed.*
