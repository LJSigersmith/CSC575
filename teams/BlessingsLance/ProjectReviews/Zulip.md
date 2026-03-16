# Project Review: Zulip (Organized chat for distributed teams)

## Getting Started

### Documents

- **[Getting Started, learning how to use Git (the Zulip way))](https://github.com/zulip/zulip/blob/main/CONTRIBUTING.md)** — Zulip uses GitHub for source control and code review, and becoming familiar with Git is essential for navigating and contributing to the Zulip codebase. They have a very **specific way** they use Git, even for experienced Git users they are still recommended to check out the Git onboarding document (**the zulip way.**) Tey have a page dedicated to introdicng you to zulip's Git-specific tools **(https://zulip.readthedocs.io/en/latest/git/zulip-tools.html)**

- **[README.md](https://github.com/zulip/zulip/blob/main/README.md)** — The repository root README gives a high-level project overview. The page contains links to the social media pages, community chat for any assistance, and points to the developer wiki. Assessment: **Clear** — good entry point to learn more about this project and how to start the onboarding process.

- **[Contribute Page](https://zulip.readthedocs.io/en/latest/contributing/contributing.html)** — This page has clear instructions on how to use their documentation to aid you in contributing to the project with the following statement highlighted, **"Reading and following our written guidelines to the very best of your ability is the only way to become a successful Zulip contributor.)**  There are clear guidelines to their policies, what they permit and what is frowned upon.

- **[GitHub Discussions](https://chat.zulip.org/#narrow/channel/1-announce/topic/docker/with/2379081)** — This is a project with active members, who are currently in th process of releasing a new version of their product to the general public. The chat is filled with question and answers, notices and updates.

### Code of Conduct
On the how to contribute page, when you click on the get started link, there are a set of rules and regulations to guide you through contributing to this open source project. They have their AI policy which is what stood out to me, it seems they do not discourage the use of AI as long as you can explain your code when asked why X=3.

### User Installation

- **[Zulip.com](https://zulip.com/help/desktop-app-install-guide)** — The product has a download page on their website which leads you to a page where you can download the installation package. On the same page there is an installation guide to guide you on how to install and run their package. The installation guide caters for the three diffeerent operating systems, MacOS, Linux and Windows.

Assessment: **Reasonable** The installation guide is easy to follow as you install the packages making it easy to use.

### Developer Installation

- **[Development Environment](https://zulip.readthedocs.io/en/latest/development/index.html)**

Installing the Zulip development environment requires downloading several hundred megabytes of dependencies, so you will need an active, reasonably fast, internet connection throughout the entire installation processes. For first-time contributors, we recommend using the Vagrant development environment on macOS and Linux based OS and WSL 2 setup on Windows. These guides will walk every developer throught the steps to setup the environment to contribute to the project. The instructions are clear an easy to flow.

Assessment: **Reasonable** —The guide makes it easy to setup the development environment with links to download the necessary tools

### Organization

Assessment: **Organized** — Highly organised project with their Git easy to navigate and find what you are looking for. Their different repositories are clearly marked and with explanations as to what that repository focuses on. There are dedicated pages depending on wether you are the user or a contributor to aid you in either using their services or contributing to their project.

### Summary                  

It feel reletively easy to get started as a contributor to this project since all the initial help you might need is already lined uo for you with clear step on how to complete each step. They ahve a well documented project which makes it easy to understand the goal and mission of the project an what they are trying to achieve long-term. 

---

## Community Communication

- **[The Zulip development community](https://zulip.com/development-community/)**
  - **Purpose:** Users and administrators of Zulip organizations stop by to ask questions, offer feedback, and participate in product design discussions.
  Contributors to the project, including the core Zulip development team, discuss ongoing and future projects, brainstorm ideas, and generally help each other out.
  - **Currency:** Actively in use currently as the project is still on-going.
  - **Activity:** Not publicly visible without an creating an account either as a new user, contributor or a self-hoster.  
  - **Responsiveness:** **Probably** — The chat seems to be active and contributors respond to each other though i wasnt able to get the sense of how fast it happens.
  - **Response Time:** Likely within hours for technical questions, based on the community's apparent activity level.
  - **Content:** Tone appears informal and collegial and respectful.

- **[GitHub Issues](https://github.com/zulip/zulip/issues)**
  - **Purpose:** Bug reports, feature requests, and project planning. Issues are assigned to contributors and serve as the primary task-tracking mechanism.
  - **Currency:** Active — new issues created regularly (multiple per week based on observed activity).
  - **Activity:** High — maintainers and contributors comment frequently on open issues.
  - **Responsiveness:** **Very likely** — Maintainers are responsive on issues, especially for bugs and assigned work.
  - **Response Time:** Hours to a few days.
  - **Content:** Technical and direct. Tone is professional. Maintainers are helpful and encourage contributors to chime in.
---

## Repositories

- **[Zulip/Zulip](https://github.com/zulip/zulip)**
  - **Purpose:** Zulip server and web application. Open-source team chat that helps teams stay productive and focused.
  - **Created:** 2016
  - **License:** (http://www.apache.org/licenses/LICENSE-2.0)

- **[Zuli/Zulip-Flutter](https://github.com/zulip/zulip-flutter)**
  - **Purpose:** Zulip mobile apps for Android and iOS, using Flutter.
  - **Created:** ~2024
  - **License:** Apache-2.0 license

- **[Zulip/Zulip-Terminal](https://github.com/freelawproject/recap-chrome)**
  - **Purpose:** Official Zulip terminal client.
  - **Created:** ~2022
  - **License:** Apache-2.0 license

- **[Zulip/Zulip-Desktop](https://github.com/zulip/zulip-desktop)**
  - **Purpose:** Zulip Desktop client for Mac, Windows and Linux.
  - **Created:** ~2016
  - **License:** Apache-2.0 license

- **[Zulip/Docker-Zulip](https://github.com/zulip/docker-zulip)**
  - **Purpose:** Container configurations, images, and examples for Zulip.
  - **Created:** ~2022
  - **License:** Apache-2.0 license

---

## Issue Tracking

- **[Zulip Issue Tracker](https://github.com/zulip/zulip/issues)**
  - **Volume:** ~1.2k open issues
    - **Approachability:** I feel this project is easy to approach due to its clear getting started guidelines. It makes it easy to setup development area to help aid in contributions and the community seems reliable when seeking help.
    - **Summary:** There are as many beginner first issues to chose from to help you navigate this project.
---

## Tools/Languages/Libraries/Frameworks

- **Tools:**
  - Docker & Docker Compose — local dev environment orchestration 
  - GitHub Actions — CI/CD pipelines (lint, test, CodeQL, Semgrep, deploy) 
  - Slack - Cloud-based instant messaging and collaboration platform 
  - Electron - desktop application framework for the development of desktop applications using front- and back-end infrastructure such as HTML, CSS, and JavaScript.
  - React Native -  JavaScript Framework for IOS an Android mobile app development.
  - LDAP server — Python dependency management — *used it*

- **Languages:**
  - Python (~57.9%) 
  - HTML (~3.6%)
  - JavaScript (~9.2%)
  - MDX (~3.1%) 
  - CSS (~4.1%) 
  - TypeScript (~18.3%) 

- **Application Libraries/Frameworks:**
  - Django — primary web framework 
  - Django REST Framework — API layer
  - Tornado — high-performance web framework or a specific class of error-correction codes
  - Webpack — powerful, open-source static module bundler for modern JavaScript applications.
  - React — used in select frontend components

- **Testing Libraries/Frameworks:**
  - Django's built-in test framework (unittest-based) 
  - Pytest

- **Summary:**Though some of the technologies used in this project I have never used before, I am confident that with the current matching skills set I can contribute to the project, I like how detailed the documentation is on getting started the issues to resolve are clearly marked especially those for first tike users.

---

## Assessment

Zulip is an exceptionally well-aligned project for me as a contributor. They are an organized chat for distributed teams, which is basically the same thing that we are trying to achieve on this course collerboaration. The technology stack is a strong match: it's primarily Python/Javascript, and I'm comfortable with some of the tooling.

**What makes this project approachable:**
Well structured documentation which makes it easy to understand the project and the goal. It has clearly marked first issues to build confidence as you start contributing to the project. The active community also encourages questions through the multiple forums that are there.

**What might make contributions harder:**
The Slack workspace is the real hub of communication, and it's not publicly accessible — a newcomer has to get an invitation. Im not too farmiliar with Tornado and Django, though im willing to learn. Im curious as to my reception from the community as I am not too familiar with some of these technologies and will be heavily reliant on the community for assistance.

**Overall:** I'm genuinely interested in this project. The combination of meaningful mission, familiar technologies, active maintainers, and clear newcomer pathways makes it the most interesting project i have reviewed. My biggest worry is the is learning these technologies in time for me to actively contribute torwads the project.

### Install Spike
> **Blessings** Will be responsible for the Install spike for **zulip**

**Getting Started**

> The guide to getting started: **https://zulip.readthedocs.io/en/latest/development/overview.html#requirements** 
> Setting up the Development ENV: **https://zulip.readthedocs.io/en/latest/development/setup-recommended.html**

add links installation 