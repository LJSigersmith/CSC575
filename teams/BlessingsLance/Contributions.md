# Project Contributions — BlessingsLance
**Project:** [Scribe-Android](https://github.com/scribe-org/Scribe-Android)

---

## Developer Install Demonstrations

| Team Member | Status | Link |
|---|---|---|
| Lance | COMPLETE | [LanceDevInstall.pptx](LanceDevInstall.pptx) |
| Blessings | COMPLETE | [Blessings_DevInstall.pptx](Blessings_DevInstall.pptx) |

---

## Active Contributions

### [Emoji Autocomplete Feature](https://github.com/scribe-org/Scribe-Android/issues/590)
- **Type:** Feature
- **Team Member:** Lance
- **Status:** In Review
- **Issue:** [scribe-org/Scribe-Android#590](https://github.com/scribe-org/Scribe-Android/issues/590)
- **PR:** [scribe-org/Scribe-Android#601](https://github.com/scribe-org/Scribe-Android/pull/601)
- **Description:** Implements colon-triggered emoji mode on the Android keyboard. Typing space + `:` activates a dedicated emoji suggestion row (6 slots on phone, 9 on tablet). Common emojis shown on bare `:`; typing after `:` prefix-matches against the `emoji_keywords` table. Tapping an emoji deletes back to the `:` and commits the selection. Space or deleting the `:` exits the mode. Mid-word colons are ignored. Changes span `GeneralKeyboardIME.kt`, `KeyHandler.kt`, `SuggestionHandler.kt`, `KeyboardUIManager.kt`, `EmojiUtils.kt`, and `input_method_view.xml`.

---

### [Emoji Keywords Table Conversion (JSON to SQLite)](https://github.com/scribe-org/Scribe-Data/issues/683)
- **Type:** Bug Fix
- **Team Member:** Lance
- **Status:** In Review
- **Issue:** [scribe-org/Scribe-Data#683](https://github.com/scribe-org/Scribe-Data/issues/683)
- **PR:** [scribe-org/Scribe-Data#684](https://github.com/scribe-org/Scribe-Data/pull/684)
- **Description:** The Scribe-Data ingestion pipeline silently skipped converting emoji keyword JSON data into the SQLite tables included in language packs because it expected Wikidata formatting. Fixed by handling emoji keyword datasets in a separate branch of the if/else logic and adjusting for the differing number of columns (emoji keywords have at most 3 columns vs. Wikidata datasets).

---

### Emoji Keywords Available in API Language Packs
- **Type:** Bug Fix
- **Team Member:** Lance
- **Status:** Waiting for community feedback
- **Issue:** N/A (discovered during investigation)
- **PR:** N/A
- **Description:** Scribe-Server's language pack update script did not include emoji keywords as a data type due to a missing Python dependency (PyICU) for Unicode processing. Identified the missing dependency and verified that adding it to the shell script allows emoji keyword processing to run. Also identified a separate bug in `generateMariaTableName` where underscores are stripped, which breaks the `emoji_keywords` table name lookup. Posted findings to the community to determine the right approach before opening a PR.

---

### Onboarding Tutorial
- **Type:** Feature
- **Team Member:** Blessings
- **Status:** In Progress
- **Issue:** N/A (based on Figma designs shared by maintainer)
- **PR:** N/A
- **Description:** Implements a guided onboarding tutorial accessible from the About tab. Five screens: Tutorial Home plus four interactive chapters (Noun Annotation, Word Translation, Verb Conjugation, Noun Plurals). Each chapter validates user keyboard input in real time with green/red feedback. Built in Kotlin with Jetpack Compose. Core files: TutorialHomeScreen.kt, TutorialStepScreen.kt, TutorialNavigator.kt, WrongKeyboardScreen.kt. Integrated into existing AboutScreen.kt.

---

#### Activity Log
| Date | Who | Event |
|---|---|---|
| 2026-04-06 | Lance | Sent intro message to Scribe-Android Matrix community: "Hi everyone! I'm Lance, a grad student at Quinnipiac University. My teammate Blessings and I have been exploring the Scribe Android codebase over the last few weeks as part of an open source software course. We would like to contribute and are looking forward to learning from the community!" |
| 2026-04-06 | Lance | Commented on [Issue 590](https://github.com/scribe-org/Scribe-Android/issues/590): Hi! I'd love to work on this if it's still available. I've looked through the relevant code and can see that SuggestionHandler and KeyHandler already lay some groundwork. It looks like the main work is wiring up colon detection, suppressing normal autocomplete while in emoji mode, and handling the space key exit. Happy to get started if it can be assigned to me! |
| 2026-04-07 | Blessings | Sent intro message to Matrix community (https://app.element.io/#/room/#ScribeAndroid:matrix.org): Hey everyone! I'm Blessings, a grad student at Quinnipiac University. I'll be working with Lance on this open source software course. Really impressed by the project and excited to get involved with the community! |
| 2026-04-07 | Blessings | Commented on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi! I'd love to work on this. I'll take a look at the Figma designs and the existing settings code to get started. Happy to pick this up if it can be assigned to me! |
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi @Mailos07 👋 We already have a PR open for this in #592. Thanks for your interest in the project. Please let us know if there's another issue that's of interest for you! We'll be unblocking more soon. |
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Thanks for your thoughts above, @Mailos07! Really interesting :) Text-to-speech for now sounds a bit out of scope. An onboarding tutorial isn't though :) See the Figma designs here for the flow that a designer made for us 😊. |
| 2026-04-08 | andrewtavis | Replied on [Issue 590](https://github.com/scribe-org/Scribe-Android/issues/590): "Ideally you two can take a look at #590 first as Lance has done some research there already. We don't have the emojis in for the full : to emoji display yet, but you two could work on it and we'll finalize the next release of Scribe-Data in the meantime 😊." |
| 2026-04-10 | Blessings | Reviewed Figma designs and identified a structured guided workflow of five screens: Tutorial Home (from About tab) plus four interactive chapters — Noun Annotation, Word Translation, Verb Conjugation, and Noun Plurals — each validating keyboard input in real time with green/red feedback. |
| 2026-04-10 | Lance | Opened [scribe-org/Scribe-Data#683](https://github.com/scribe-org/Scribe-Data/issues/683): "Emoji keyword data conversion from JSON to sqlite fails" — identified `AttributeError: 'list' object has no attribute 'keys'` in `data_to_sqlite.py` line 324 when processing emoji_keywords JSON. |
| 2026-04-10 | Lance | Opened [scribe-org/Scribe-Data#684](https://github.com/scribe-org/Scribe-Data/pull/684): "Fix emoji_keywords not being generated in SQLite export" — excludes emoji_keywords from standard dict-based processing and fixes emoji loop with `min(len(json_data[row]), len(cols) - 1)` to prevent IndexError. All 378 tests pass. |
| 2026-04-11 | Blessings | Began implementing the tutorial system in Kotlin/Jetpack Compose. Created TutorialHomeScreen.kt, TutorialStepScreen.kt, TutorialNavigator.kt, and WrongKeyboardScreen.kt. Integrated into AboutScreen.kt via state-driven toggle. Resolved build errors including an incompatible icon reference and a validation logic issue. Tutorial compiles, renders on emulator, and supports light/dark themes. |
| 2026-04-11 | Lance | Sent message to Scribe-Data Matrix community: "Hi everyone! I've been working on an issue in Scribe-Android with emoji suggestions, and noticed the emoji_keywords table was not included in downloaded language packs. I traced this back to a bug in Scribe-Data causing a crash when processing emoji keywords. I opened PR #684 to fix this. I also noticed that update_data.sh doesn't currently include the emoji_keywords data type and I see issue 43 mentions this. I was able to generate emoji_keywords locally by adding apt-get install -y libicu-dev pkg-config g++ python3-dev to the workflow which is needed for PyICU's Unicode processing. Wanted to check: is adding these dependencies to the GitHub workflow dependencies and adding emoji_keywords to the data types in update.sh the right approach for getting emoji_keywords into the language packs? Happy to open a PR for Scribe-Server if I'm on the right track!" |
| 2026-04-14 | Blessings | Commented on conjugation bug issue: flagged that the Verb Conjugation chapter of the tutorial is blocked by the conjugation bug; will adapt implementation once a fix is in place. |
| 2026-04-20 | Lance | Opened [scribe-org/Scribe-Android#601](https://github.com/scribe-org/Scribe-Android/pull/601): "Feature: Colon to Emoji Functionality" — implements emoji colon mode with 6-slot phone / 9-slot tablet suggestion row, prefix matching against emoji_keywords table, common emojis on bare `:`, and space/delete exit. |
| 2026-04-20 | Lance | Sent message to Scribe-Android Matrix community: "Hey everyone! I've opened a PR implementing emoji colon mode for Scribe-Android (#590). Typing : triggers a dedicated emoji search row in the suggestion bar — 6 slots on phone, 9 on tablet — with prefix matching against the emoji_keywords table and a set of common emojis shown on the bare :. Getting this working end-to-end also surfaced issues in two other repos: Scribe-Data — PR #684 fixes a column overflow bug in data_to_sqlite.py that was preventing emoji_keywords from being written to SQLite. Scribe-Server — emoji_keywords needs to be added to the data pipeline and an underscore-stripping issue in generateMariaTableName needs a fix. Would love any feedback!" |

---

## Potential Contributions
| Title | Type | Issue | Assigned To | Notes |
|---|---|---|---|---|
| Add emoji_keywords to Scribe-Server language pack pipeline | Bug Fix / Feature | [scribe-org/Scribe-Server#43](https://github.com/scribe-org/Scribe-Server/issues/43) | Lance | Awaiting community feedback on approach — add PyICU dependencies to update_data.sh and include emoji_keywords as a data type. Would unblock the Emoji Autocomplete Feature. |
---

## Completed Contributions

| Title | Type | PR | Merged By | Date |
|---|---|---|---|---|
| — | — | — | — | — |

---

## Abandoned Contributions

| Title | Reason | Date Abandoned |
|---|---|---|
