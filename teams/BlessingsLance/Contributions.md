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
- **Status:** Blocked (pending emoji keywords in language packs)
- **Issue:** [scribe-org/Scribe-Android#590](https://github.com/scribe-org/Scribe-Android/issues/590)
- **PR:** N/A
- **Description:** Adds colon-triggered emoji autosuggestion to the Android keyboard. Typing `:` activates emoji mode, suppressing normal autocomplete and showing common emojis. Typing text after `:` filters results. Selecting an emoji replaces the colon and typed text. Space exits emoji mode. Blocked on emoji keywords being available in downloaded language packs (see Contributions 2 & 3).

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
- **Description:** Scribe-Server's language pack update script did not include emoji keywords as a data type due to a missing Python dependency (PyICU) for Unicode processing. Identified the missing dependency and verified that adding it to the shell script allows emoji keyword processing to run. Posted findings to the community to determine whether the dependencies should be added to the update script or to the pipeline dependencies.

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
| 2026-04-06 | Lance | Commented on [Issue 590](https://github.com/scribe-org/Scribe-Android/issues/590): Hi! I'd love to work on this if it's still available. I've looked through the relevant code and can see that SuggestionHandler and KeyHandler already lay some groundwork. It looks like the main work is wiring up colon detection, suppressing normal autocomplete while in emoji mode, and handling the space key exit. Happy to get started if it can be assigned to me!
| 2026-04-07 | Blessings | Sent intro message to Matrix community (https://app.element.io/#/room/#ScribeAndroid:matrix.org): Hey everyone! I'm Blessings, a grad student at Quinnipiac University. I'll be working with Lance on this open source software course. Really impressed by the project and excited to get involved with the community! |
| 2026-04-07 | Blessings | Commented on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi! I'd love to work on this. I'll take a look at the Figma designs and the existing settings code to get started. Happy to pick this up if it can be assigned to me!
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi @Mailos07 👋 We already have a PR open for this in #592. Thanks for your interest in the project. Please let us know if there's another issue that's of interest for you! We'll be unblocking more soon. I have to find another issue to work on.|
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): andrewtavisThanks for your thoughts above, MMailos07! Really interesting :) Text-to-speech for now sounds a bit out of scope. An onboarding tutorial isn't though :) See the Figma designs here for the flow that a designer made for us 😊.|
| 2026-04-08 | andrewtavis | Replied on [Issue 590](https://app.element.io/#/room/#ScribeAndroid:matrix.org): "Ideally you two can take a look at #590 first as Lance has done some research there already. We don't have the emojis in for the full : to emoji display yet, but you two could work on it and we'll finalize the next release of Scribe-Data in the meantime 😊." |
| 2026-04-10 | Lance | Opened [scribe-org/Scribe-Data#683](https://github.com/scribe-org/Scribe-Data/issues/683): "Emoji keyword data conversion from JSON to sqlite fails" — identified `AttributeError: 'list' object has no attribute 'keys'` in `data_to_sqlite.py` line 324 when processing emoji_keywords JSON. |
| 2026-04-10 | Lance | Opened [scribe-org/Scribe-Data#684](https://github.com/scribe-org/Scribe-Data/pull/684): "Fix emoji_keywords not being generated in SQLite export" — excludes emoji_keywords from standard dict-based processing and fixes emoji loop with `min(len(json_data[row]), len(cols) - 1)` to prevent IndexError. All 378 tests pass. |
| 2026-04-11 | Lance | Sent message to Scribe-Data Matrix community: "Hi everyone! I've been working on an issue in Scribe-Android with emoji suggestions, and noticed the emoji_keywords table was not included in downloaded language packs. I traced this back to a bug in Scribe-Data causing a crash when processing emoji keywords. I opened PR #684 to fix this. I also noticed that update_data.sh doesn't currently include the emoji_keywords data type and I see issue 43 mentions this. I was able to generate emoji_keywords locally by adding apt-get install -y libicu-dev pkg-config g++ python3-dev to the workflow which is needed for PyICU's Unicode processing. Wanted to check: is adding these dependencies to the GitHub workflow dependencies and adding emoji_keywords to the data types in update.sh the right approach for getting emoji_keywords into the language packs? Happy to open a PR for Scribe-Server if I'm on the right track!" |
| 2026-04-10 | Blessings | After reviewing the Figma designs for the Scribe project, I identified a structured guided workflow consisting of five main screens: a Tutorial Home screen accessible from the About tab, along with four interactive chapters covering Noun Annotation, Word Translation, Verb Conjugation, and Noun Plurals. Each chapter is designed to have the user interact directly with the Scribe keyboard while validating their input in real-time, displaying green success messages when correct or red error prompts when incorrect. |
| 2026-04-08 | Blessings | Following the Figma review, I began implementing the tutorial system in Kotlin using Jetpack Compose. I created four core files: **TutorialHomeScreen.kt** for the tutorial landing page with the chapter list and 'Start full tutorial' button **TutorialStepScreen.kt** as the reusable interactive lesson component with input validation **TutorialNavigator.kt** to manage the navigation flow between chapters and steps **WrongKeyboardScreen.kt** to handle cases where a non-Scribe keyboard is active. I integrated the tutorial into the existing **AboutScreen.kt** by adding a state-driven toggle that switches between the About content and the tutorial flow when the user taps the tutorial button. During testing on the emulator, I resolved several build errors including an incompatible icon reference and a validation logic issue that was blocking users from progressing through the instructional chapters. The tutorial currently compiles, renders on the emulator, and supports both light and dark themes, though further refinement is needed to fully connect the interactive exercises with the live Scribe keyboard.
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
