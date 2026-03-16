# Scribe-Android Developer Environment Setup

## Prerequisites

- **Android Studio** — Download from https://developer.android.com/studio
- **Git** — With submodule support
- **Python 3** — Required for pre-commit hooks

---

## 1. Clone the Fork with Submodules

The repo includes `Scribe-i18n` as a git submodule (`app/src/main/assets/i18n`). If you clone without `--recurse-submodules`, the localization files will be missing.

```bash
git clone --recurse-submodules https://github.com/LJSigersmith/Scribe-Android.git
cd Scribe-Android
```

If you already cloned without the flag, initialize manually:

```bash
git submodule update --init --recursive
```

---

## 2. Add the Upstream Remote

To keep the fork in sync with the original Scribe project:

```bash
git remote add upstream https://github.com/scribe-org/Scribe-Android.git
git remote -v   # verify
```

Expected output:
```
origin    https://github.com/LJSigersmith/Scribe-Android.git (fetch)
origin    https://github.com/LJSigersmith/Scribe-Android.git (push)
upstream  https://github.com/scribe-org/Scribe-Android.git  (fetch)
upstream  https://github.com/scribe-org/Scribe-Android.git  (push)
```

To pull upstream changes later:

```bash
git fetch upstream
git merge upstream/main
git submodule update --init --recursive
```

---

## 3. Install Pre-commit Hooks

Pre-commit hooks enforce formatting, linting (ktlint, detekt), and license headers on all `.kt` files before each commit.

On macOS, `pip` may not be on your PATH — use `pip3`:

```bash
pip3 install --upgrade pip pre-commit
pre-commit install
```

> **Note:** If `pre-commit` is not on your PATH after install, it lands in `~/Library/Python/3.x/bin/`. Either add that to your `PATH` or invoke it directly:
> ```bash
> /Users/<you>/Library/Python/3.9/bin/pre-commit install
> ```

The hooks configured in `.pre-commit-config.yaml` are:

| Hook | What it does |
|---|---|
| `trailing-whitespace` | Removes trailing whitespace in `.kt` files |
| `end-of-file-fixer` | Ensures `.kt` files end with a newline |
| `check-yaml` | Validates YAML syntax |
| `spdx-license-checker` | Enforces `GPL-3.0-or-later` SPDX header |
| `formatKotlin` | Auto-formats Kotlin via `./gradlew formatKotlin` |
| `ktlint` | Lints Kotlin via `./gradlew lintKotlin` |
| `detekt` | Static analysis via `./gradlew detekt` |

---

## 4. Open in Android Studio

1. Open **Android Studio**
2. Choose **Open** and select the `Scribe-Android` directory
3. Let Gradle sync complete (Android Studio will prompt automatically)
4. If caches seem stale after a pull: **File → Invalidate Caches… → Invalidate and Restart**

---

## 5. Set Up an Emulator

1. Open **Device Manager** (toolbar icon or **View → Tool Windows → Device Manager**)
2. Click **Create Device**
3. Choose a hardware profile (e.g., Pixel 6) and a system image (API 33+ recommended)
4. Finish and start the virtual device

---

## 6. Select a Build Variant

The project has two build variants. Select one via **Build → Select Build Variant**:

| Variant | App |
|---|---|
| `keyboardDebug` | Scribe Language Keyboards (default) |
| `conjugateDebug` | Verb conjugation app |

---

## 7. Run the App

Press the **Run ▶** button (or `Shift + F10`) with your emulator running.

---

## Repository Structure Notes

```
Scribe-Android/
├── app/
│   └── src/main/assets/i18n/   # Scribe-i18n submodule (localization)
├── .pre-commit-config.yaml      # Pre-commit hook definitions
├── build.gradle.kts             # Top-level Gradle build file
├── detekt.yml                   # Detekt static analysis config
├── CONTRIBUTING.md              # Contribution guidelines
└── scripts/                     # Utility scripts
```

---

## Links

- [Scribe-Android upstream repo](https://github.com/scribe-org/Scribe-Android)
- [CONTRIBUTING.md](https://github.com/scribe-org/Scribe-Android/blob/main/CONTRIBUTING.md)
- [Android Studio download](https://developer.android.com/studio)
- [Scribe community (Matrix)](https://matrix.to/#/#scribe_community:matrix.org)