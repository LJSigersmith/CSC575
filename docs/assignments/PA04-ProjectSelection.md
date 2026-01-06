## PA04 - Project Ranking and Selection

### Introduction

Through the [Project Explorations](PA02-ProjectExplorations.md) and [Project Reviews](PA03-ProjectReviews.md) you have all gained a great deal of familiarity with a wide variety of H/FOSS projects. This assignment asks you to form a project team, make a direct comparison between a number of the projects in which the team is interested, and based on that comparison select the H/FOSS project on which the team will work for the year.

### Team Formation

Your instructor will use the information from the explorations and reviews that have been posted on the Course Repository to identify common areas of interest across the class.  During class time, these areas will be presented and individuals will indicate their interest in working on different projects.  We as a class will then negotiate the exact composition of each project team such that everyone has been placed on a team in which they have some shared interest.  Each team will have between 2 and 5 members and an effort will be made to keep the total number of teams in the class to 5 or less. Keep in mind that during the actual project work, teams may divide into smaller groups (sub-teams of two or three) as appropriate to work on different aspects of the same H/FOSS project.

### Assignment

Once the teams have been formed, each team will complete the Ranking and Selection activities below in order to choose the project on which they will work. There will be one submission for this assignment for each project team. The submission must be completed collaboratively with the involvement of all team members.

To complete this assignment:

1. Determine at least two times during the week when all members of the team can meet to hold out-of-class meetings.
2. Using one team member's fork/clone of the course repo:
   1. Create a feature branch for the team's work 
   2. Create a directory for your team in the `teams` directory.
   3. Create a `README.md` file in your team's directory.
   4. Copy the `ProjectSelection.md` file in the `teams` directory into your team's folder.
   5. Compete the following tasks to add content to your team's `README.md`
      1. Add a top level heading to the `README.md` containing the the text "Our Team".
      2. Add a "Team Members" subheading followed by a list with the names of all team members that link to their individual `README.md` files.
      3. Add a "Meeting Times" subheading followed by at least two times outside of class time that all members of the team are available to meet.
      3. Add a "Project Documents" subheading.
      4. Add a bullet to the "Project Documents" section that links to the copy of `ProjectSelection.md` file in your team's folder.
   6. Complete the following tasks to add content to the team's `ProjectSelection.md` document for this assignment.
      1. Complete the [Projects Considered](#projects-considered) section below.
      2. Complete the [Install Spike](#install-spike) section below.
      3. Complete the [Project Ranking](#project-ranking) section below.
      4. Complete the [Project Selection](#project-selection) section below.
      5. Choose a name for the team and update the "Our Team" top level heading in the `README.md` file to be the team's name.
   7. Create a PR to the upstream course repo containing the team's work for this assignment.

#### Projects Considered

Have a discussion within the team about all of the projects that the team members have reviewed. This discussion should last no more than 1 hour, but must ensure that every team member has an equal opportunity to discuss the projects in which they are interested.

Based on this discussion decide on at least 3 projects that the team will consider for selection as their project for the year. It is highly recommended that every projects being considered has been reviewed by at least one of the team's members.

For each project that the team is considering for selection:
1. Edit one of the bullets in the "Projects Considered" section of your team's `ProjectSelection.md` file to give information about the project.
3. Add links to of all of the Project Explorations and Project Reviews that were completed (including those not done by your classmates). You can find these links on the [Project Explorations](https://github.com/Dickinson-COMP-491-492/AY25-26/blob/main/projectExpl.md) and [Project Reviews](https://github.com/Dickinson-COMP-491-492/AY25-26/blob/main/projectRev.md) pages in the Course Repository.

Note, the team may find that as its discussion progress it makes sense to come back and consider different or additional projects. That is perfectly acceptable, just add them to the list accordingly.

#### Install Spike

As a part of the Project Explorations and Project Reviews the team members have looked at the documentation for installing, running and working on these projects.  However, it is often not until you really attempt to install and work on the project that it becomes clear how helpful (or not) this documentation is.  The spike in this section will help the team to more fully evaluate how easy or how difficult it might be to get started as a developer with the project.

For each project being considered:
   1. Update one of the "Project Name" subsections in the "Install Spike" section of your team's `ProjectReviews.md` file.
   2. Assign a sub-set of the team's members to be responsible for the install spike for that project.
   2. The sub-set of team members assigned to each project will then complete the <!--[User Perspective Spike](#user-perspective-spike) and the--> [Developer Perspective Spike](#developer-perspective-spike) for the project as described below.

<!--
##### User Perspective Spike

The purpose of this spike is to get a feel for what it would be like as a user coming to the product. You will want to find and use the directions that the project provides for new users wanting to install/use the product. This may require you to download and install an executable program, or there may be a live demo available online, or you may have to build the executable program from its source code. If there are multiple ways to install the product as a user, you should choose what seems like the easiest way.

To complete the User Perspective Spike:
1. Spend a maximum of 1 hour trying to install/use the latest version of the product as a user.  If you are unable to install/use the program within 1 hour stop.
2. In the "Install Spike" section for the project update the "User Install Spike" information by:
   1. Adding links to any "Installation Documents" that you found useful when attempting to install/use the product.
   2. Adding links to any "Download/Demo Sites/Repos" that you used.
   3. Adding a "Summary" paragraph describing your experience trying to install/run the program as a user. Your summary should include information about whether you were successful or not in running/using the program, how you ran the program (installed an executable/used a live demo/etc...), your assessment of the quality of the documentation that you used, how difficult you found the installation, and a discussion of any difficulties you experienced.
-->

##### Developer Perspective Spike

The purpose of this spike is to get a feel for what it will be like to get setup to contribute to this project. You will want to find the directions that the project provides for getting set up to modify the code of the project. This will definitely require forking and cloning the project repository, among other steps.  Often projects will have documents about "getting started", "how to contribute", "developer install", or something similar. You may need to dig around a little to find the appropriate documentation. If you are having difficulty finding the relevant information for your project see your instructor for assistance.

To complete the Developer Perspective Spike:
1. Spend a maximum of 5 hours trying to install the development environment and getting the product to build and run from the source code.  If you are unable to install the development environment, and build and run the product from the source code within 5 hours stop.
2. In the "Install Spike" section for the project, update the "Developer Install Spike" information by:
   1. Adding links to any "Installation Documents" that you found useful when attempting to install/build/run the product from the source code.
   2. Adding links to your fork and the project's upstream repository to the "Repository Links" bullet.
   3. Adding a "Summary" paragraph summarizing your experience trying to install/build/run the program as a developer. Your summary should include information about whether you were successful or not in installing/building/running the program, your assessment of the quality of the documentation that you used, how difficult you found it to install/build/run the program, and a discussion of any difficulties you experienced.

#### Project Ranking

Once the team has completed the Install Spikes, it will create rankings for the projects being considered.  Information including the Project Explorations, Project Reviews, the Install Spikes, and the team members' backgrounds and interests will factor into these rankings. The team must ensure that all team members have equal voice in this conversation.

To complete the Project Ranking:

1. Replace P1, P2, P3 in the "Project Name" column in the table in the "Project Rankings" section with the names of the projects your team is considering. Add additional rows to the table as necessary.
2. Engage in a full team discussion of the Project Explorations, Project Reviews, Install Spikes and any other information you find useful to come to a consensus ranking for the projects along each of the dimensions described below. Each project should get a ranking  for each dimension (1, 2, 3, ... with 1 being the best). Ties are allowed.
   - **Community**: *How would it be to work within this project's community?* Consider issues including the size and diversity of the user and developer communities, the availability and variety of communication channels, the quality and tone of communications, and how the community treats and on-boards newcomers.
   - **Complexity**: *How technically hard is it going to be to work on this project?* Consider issues including your ability to grasp the overall purpose and organization of the project, size of the code base, the number of different tools/languages/technologies/frameworks used, the quality of documentation, and the modularity of the project (i.e. will you be able to isolate what you have to know?).
   - **Activity**: *How active is this project?* Consider issues including the recent responsiveness of community members in the communication channels, the rate at which the code is changing (is it too slow or too fast?), whether new issues are being opened, commented on and closed, whether pull requests are receiving feedback and being merged, and how up to date the documentations is.
   - **Approachability**: *How hard would it be to get started with this project?* Consider issues including the quality of the getting started documentation for contributors, your experiences with the Install Spike, the number of new contributors that have contributed to the project recently, availability and understandability of good first issues, alignment of your team's current skill set with the project's tools/languages/technologies/frameworks, and the amount of domain knowledge required.
   - **Appeal**: *How interested is your team in this project?* Consider issues including the application domain, the benefits to end users, the technologies employed, and the goals of the team members.
3. Complete the "Rationale" section by giving a paragraph for each dimension that summarizes the team's rationale for the rankings in that dimension. The paragraph for each dimension should be comparative. It should use details from the team's discussion of the Project Explorations, Project Reviews and the Install Spikes to make it clear why projects were ranked higher or lower than others on the dimension.

#### Project Selection

Engage in a full team discussion of the rankings and rationale that you produced in the prior section with the goal of selecting the project on which the team will work. The rankings are to help inform the team's decision but it is not required that you simply choose the highest ranked project. For example, the team might weigh different dimensions more heavily than others in its decision making. The team must ensure that all team members have an equal voice in this conversation.

When the team has selected a project complete the "Project Selection" section as follows:

1. Indicate the "Project" that the team selected.
2. Give a paragraph explaining the "Rationale" for the team's choice.  This should describe the team's thinking, including how it considered the rankings, which dimensions it weighed most heavily and why.
3. Review the team's experiences with the Install Spike for the selected project and give rough "Install Estimate" for how many hours it might take all team members to get the product up and running as a developer.
4. List, with a brief explanation, any "Knowledge Gaps" that the team thinks it has and needs to fill in before beginning work on this project. For example, what tools/languages/frameworks will the team members need to learn?
5. List, with a brief explanation, any additional "Concerns" that the team has about working on the selected project.

### Acknowledgements

This assignment builds from and adapts ideas and content from the following activities created by others:

* https://github.com/ChrisMurphyOnline/open-source-software-development-course/blob/master/activities/foss-evaluation-activity.txt
* http://foss2serve.org/index.php/Project_Evaluation_Activity_V2

---

![Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License") All textual materials used in this course are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

![GPL V3 or Later](https://www.gnu.org/graphics/gplv3-or-later-sm.png "GPL V3 or later") All executable code used in this course is licensed under the [GNU General Public License Version 3 or later](https://www.gnu.org/licenses/gpl.txt)
