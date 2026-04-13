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

### Title
- **Type:** Bug Fix / Feature / Documentation / Translation / UI / Other
- **Team Members:** Lance/Blessings
- **Status:** Identified / In Progress / In Review / Merged / Abandoned
- **Issue:** ###
- **PR:** *if applicable*
- **Description:** Description

#### Activity Log
| Date | Who | Event |
|---|---|---|
| 2026-04-06 | Lance | Sent intro message to Matrix community: Hi everyone! I'm Lance, a grad student at Quinnipiac University. My teammate Blessings and I have been exploring the Scribe Android codebase over the last few weeks as part of an open source software course. We would like to contribute and are looking forward to learning from the community! |
| 2026-04-06 | Lance | Commented on [Issue 590](https://github.com/scribe-org/Scribe-Android/issues/590): Hi! I'd love to work on this if it's still available. I've looked through the relevant code and can see that SuggestionHandler and KeyHandler already lay some groundwork. It looks like the main work is wiring up colon detection, suppressing normal autocomplete while in emoji mode, and handling the space key exit. Happy to get started if it can be assigned to me!
| 2026-04-07 | Blessings | Sent intro message to Matrix community (https://app.element.io/#/room/#ScribeAndroid:matrix.org): Hey everyone! I'm Blessings, a grad student at Quinnipiac University. I'll be working with Lance on this open source software course. Really impressed by the project and excited to get involved with the community! |
| 2026-04-07 | Blessings | Commented on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi! I'd love to work on this. I'll take a look at the Figma designs and the existing settings code to get started. Happy to pick this up if it can be assigned to me!
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): Hi @Mailos07 👋 We already have a PR open for this in #592. Thanks for your interest in the project. Please let us know if there's another issue that's of interest for you! We'll be unblocking more soon. I have to find another issue to work on.|
| 2026-04-08 | andrewtavis | Replied on [Issue 562](https://github.com/scribe-org/Scribe-Android/issues/562): andrewtavis
Thanks for your thoughts above, MMailos07! Really interesting :) Text-to-speech for now sounds a bit out of scope. An onboarding tutorial isn't though :) See the Figma designs here for the flow that a designer made for us 😊.|
| 2026-04-08 | andrewtavis | Replied on [Issue 590](https://app.element.io/#/room/#ScribeAndroid:matrix.org): andrewtavis
Ideally you two can take a look at #590 first as Lance has done some research there already. We don't have the emojis in for the full : to emoji display yet, but you two could work on it and we'll finalize the next release of Scribe-Data in the meantime 😊.|
| 2026-04-10 | Blessings | After reviewing the Figma designs for the Scribe project, I identified a structured guided workflow consisting of five main screens: a Tutorial Home screen accessible from the About tab, along with four interactive chapters covering Noun Annotation, Word Translation, Verb Conjugation, and Noun Plurals. Each chapter is designed to have the user interact directly with the Scribe keyboard while validating their input in real-time, displaying green success messages when correct or red error prompts when incorrect. |
| 2026-04-08 | Blessings | Following the Figma review, I began implementing the tutorial system in Kotlin using Jetpack Compose. I created four core files: 
**TutorialHomeScreen.kt** for the tutorial landing page with the chapter list and 'Start full tutorial' button. 
**TutorialStepScreen.kt** as the reusable interactive lesson component with input validation. 
**TutorialNavigator.kt** to manage the navigation flow between chapters and steps.
**WrongKeyboardScreen.kt** to handle cases where a non-Scribe keyboard is active. 

I integrated the tutorial into the existing **AboutScreen.kt** by adding a state-driven toggle that switches between the About content and the tutorial flow when the user taps the tutorial button. During testing on the emulator, I resolved several build errors including an incompatible icon reference and a validation logic issue that was blocking users from progressing through the instructional chapters. The tutorial currently compiles, renders on the emulator, and supports both light and dark themes, though further refinement is needed to fully connect the interactive exercises with the live Scribe keyboard.
---

## Potential Contributions

| Title | Type | Issue | Assigned To | Notes |
|---|---|---|---|---|
| Add colon (:) to emoji functionality to the Android keyboard app | Feature | [#590](https://github.com/scribe-org/Scribe-Android/issues/590) | Lance | Groundwork for Emoji detection mostly done, just need to add the feature and it seems straightforward enough |
| Creation of Conjugate app Settings tab | Feature | [#562](https://github.com/scribe-org/Scribe-Android/issues/562) | Blessings | This task is well-suited for a new contributor since it primarily involves reusing and simplifying existing settings code from the keyboard app rather than building anything from scratch, with clear Figma designs to follow. The difficulty level is moderate, understanding the codebase structure will take some initial effort, but with the maintainer's support, it's achievable.
---

## Completed Contributions

| Title | Type | PR | Merged By | Date |
|---|---|---|---|---|
| — | — | — | — | — |

---

## Abandoned Contributions

| Title | Reason | Date Abandoned |
|---|---|---|
| — | — | — |
