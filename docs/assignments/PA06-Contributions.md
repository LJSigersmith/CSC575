## PA06 - Project Contributions

### Introduction

For the remainder of the course teams will be working on making contributions to the project communities that they have selected. These contributions will vary significantly by project, by team, and even within teams. Each team's job is to find ways to contribute that match the needs and priorities of the community, and the skills and interests of the team members. Contributions might include bug fixes, new features, documentation, translation, UI/UX design, and a wide variety of other technical and non-technical things. It is however, expected that at some point before the end of the course every member of every team will have worked on a technical contribution (i.e. something to do with code).

### Assignment

This assignment has two components that are to be worked on concurrently: 

1. The team will need to identify contributions on which they will work and maintain a page in the course repository documenting their progress toward making those contributions. This component will be ongoing for the remainder of the course. If an identified contribution is completed (or abandoned), then a new contribution should be identified and pursued.
  - The [Identifying Potential Contributions](#identifying-potential-contributions) and the [Documenting Project Contributions](#project-contributions) sections provide more information on this component.
2. All team members must successfully complete the developer install for the project and individually demonstrate that their installation is working. 
  - The [Demonstrating the Developer Install](#demonstrating-the-developer-install) section below describes how this is to be done.

#### Identifying Potential Contributions

The team should identify a number of potential contributions that the members of the team are interested in working on. These may be contributions that the team will work on together, or they may be contributions that smaller sub-teams or pairs will work on in parallel. This will depend on the team's members and the contributions that are found. The exact division is up to the team. However, every team member will need to be associated with at least one potential contribution at all times.

There are a number of good ways to identify potential contributions and all should be pursued:
- Review the project's contributing documentation and follow any suggestions that are given.
- Review the project's communication channels for any messages from others who are/were getting started and read the relevant responses.  This can also help to inform you about which project maintainers that are most involved in onboarding new contributors or interacting with student teams. It may be helpful to then search for more messages from those maintainers.
- Use an appropriate communication channel to introduce your team to the community and ask for guidance.
  - When reaching out to the community, be sure that you explain that you are a team of senior undergraduate computer science students in a year-long capstone course that focuses on open source contribution. You might mention that the course continues through May and that you will be spending approximately 6-8 hours per week on the project work. Then ask directly for suggestions, tips or pointers to good places to start. 
- Browse the issue tracker for issues that seem interesting and approachable to your team. If you settle on an issue you intend to work on follow the project's conventions for letting them know.  Some projects will ask you to comment on the issue. Others would like to to create a draft pull request. Others simply prefer that you start working on it and get in touch if you have questions.  In any case, you should feel free to reach out to the community about the issue you are working on if you have any questions about the issue or how to get started on it.
- If you are having difficulty identifying potential contributions or figuring out how to connect with your project community you should talk with your instructor.

As you identify potential contributions, document them as described in the [Documenting Project Contributions](#documenting-project-contributions) section below. 

#### Documenting Project Contributions

Teams will create a document in the course repository that tracks their active and potential future contributions.

1. Make a copy of the `ProjectContributions.md` file from the `teams` directory in the course repository into the team's own directory.
2. Add a bullet to the “Project Documents” section of the team's `README.md` that links to the team’s `ProjectContributions.md` file.
3. Fill in the template in the `ProjectContributions.md` file with information about the potential contributions that you have identified.
4. Create a pull request containing your changes to the upstream course repository.

This document must be created and every team member must be associated with at least one active contribution by the assignment due date.

This document must continue to be updated and maintained throughout the remainder of the course. Any time there is a significant event (issue, comment, posting, commit, pull request, merge, etc.) the team must update the `ProjectContributions.md` file and create a new PR to the upstream. Activity recorded in this document will be accounted for in your [Project Effectiveness](./PE-ProjectEffectiveness.md) scores.  **Teams should make keeping this document up to date a part of their weekly team meetings.**

#### Demonstrating the Developer Install

Having a working developer install that allows code changes to be made and tested locally is a prerequisite to working on technical contributions. Each team member is required to individually demonstrate that their development environment is working. This demonstration is to be submitted by sharing a narrated screen recording of the steps outlined below.

See the following resources for information on how to create screen recordings:
- [How to record the screen on your Mac](https://support.apple.com/en-us/102618) - Use the QuickTime Player section to record audio.
- [Record Screen with Snipping Tool app in Windows 11](https://www.elevenforum.com/t/record-screen-with-snipping-tool-app-in-windows-11.11190/).
- [Using Zoom to Create Quick and Easy Screen Recordings](https://blog.smu.edu/itconnect/2017/08/23/using-zoom-create-quick-easy-screen-recordings-free/).
- [How to use OBS Screen Capture](https://restream.io/learn/obs-studio/how-to-use-obs-screen-capture/).

Here are a few examples of screen recordings of demonstrations that illustrate the style that is expected.  Notice in particular that the author gives a detailed narration of the actions and discusses what is happening at each point. Also note how the mouse pointer and highlighting are used to make it clear which part of the screen is being discussed at relevant times.
- [VS Code Tips - Quick search](https://www.youtube.com/watch?v=pL7JKHcHcjs) (1:31)
- [Markdown Tips - Vertical Spacing in lists and understanding loose vs tight lists](https://www.youtube.com/watch?v=5DpWN2T3ASs) (7:37)

Your recorded demonstration must clearly perform each of the following steps while narrating them in your own voice:
1. Show that you are on the main development branch of the project.
2. Build and run the program from the main development branch.
3. Demonstrate the current behavior of the program that will be changed in step #4.
4. Switch to a feature branch that includes a change to the behavior of the program.
   - The feature branch and the change should be made in advance of recording the demo.
   - The change must be one that requires a rebuild of the program in order to take effect.
   - This change will ideally be related to a contribution that you are working on. If that is not possible, it may instead be a small but observable change that is made just for the purposes of the demonstration.
5. Show and briefly discuss the source code for the change that has been made.
6. Build and run the program from the feature branch.
7. Demonstrate the change.

Send your recording in a direct message to the instructor in Teams before the assignment due date.

---

![Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License") All textual materials used in this course are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

![GPL V3 or Later](https://www.gnu.org/graphics/gplv3-or-later-sm.png "GPL V3 or later") All executable code used in this course is licensed under the [GNU General Public License Version 3 or later](https://www.gnu.org/licenses/gpl.txt)