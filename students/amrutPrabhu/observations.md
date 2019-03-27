# Project: [NUSMods](https://github.com/nusmodifications/nusmods/)

NUSMods is an unofficial module planning platform for National University of Singapore (NUS), and is practically used by all NUS students. Currently, it offers a semester timetable planner, module information bank, and a venue locator and availability checker.

## NUSMods Contribution Guide

Here is an overview of the parts of the NUSMods Contribution guide.

- The project README links to the 5 subprojects that make up the NUSMods repository. Each of these **subprojects have their own READMEs** (with varying levels of completeness) that highlights what the subproject is about, the processes involved, and how to get started with contributing to it.

- The document also provides links to the NUSMods communication channels, the main one being Telegram. The community is active on Telegram and have **open discussions** about the project direction and design choices, apart from providing updates about new features.

- The Contributing section has the typical elements: Code of Conduct, Setting up Guide, Development Worflow. The details provided are comprehensive, yet to-the-point. 
	- The project is easy to setup as subproject-specific details are provided and no project configuration or external tools (apart from standard ones like Node and Yarn) are _required_.
	- In order to fix an issue, it is recommended to state your interest in taking up the issue. This is to prevent other contributors from working on the same issue. The documentation also specifically states that if you don't follow up on it for **more than two weeks**, others can take up the issue.

## Comparison between processes of NUSMods and TEAMMATES

This section provides more specific details about the NUSMods process and practices, by comparing it with the one used by TEAMMATES.

### Differences

- Netlify is part of the CI checks. Hence, each PR comes with a **deployed website preview** with the changes made. This allows reviewers and contributors to see the bug fix or feature in action, without needing to locally deploy the changes made in the PR. 

- NUSMods also uses the [Renovate](https://github.com/marketplace/renovate) bot to **automate dependency management**. It creates new PRs when a new version of a project dependency is released. TEAMMATES doesn't have any such process. In fact, it is done manually and only on a need to basis- when a released version has a new feature or introduces several big changes, for example.  

- NUSMods uses Webpack to resolve most TypeScript **import paths to absolute path**, instead of relative paths like the ones in TEAMMATES.

- NUSMods only a **handful number of active contributors** since it has a smaller target audience, i.e., NUS students. They don't use labelling for PRs (like toReview, finalReview). TEAMMATES regularly gets a lot of contributors who generally fix a couple of issues. In addition, there are dedicated groups of contributors who work on subprojects, owing to CS3282.

- As a result of the previous point, NUSMods does not extensively use labels for PRs. Since they only have a couple of project maintainers, an extensive labelling system may be overkill too. 

- NUSMods uses **Telegram and the GitHub issue tracker** as their primary communication channels. Uncertain features are discussed in depth in the corresponding GitHub issue so that potential contributors have an idea of how to go about resolving the issue. The Telegram group is used for requesting for help with small problems, informing members about minor updates, and some review requests.  

### Similarities

- Like TEAMMATES, NUSMods has GitHub issue templates for reporting bugs and requesting features. This helps standardise issue formats and also guides the authors in terms of what  information needs to be provided to make the issue complete.

- Both projects use the forking worflow with regards to PRs. Though maintainers have push access to the repository, they do not push directly to the `master` branch. Their contributions are still subjected to the same review process.

## Suggestions for TEAMMATES

After my experience contributing to the NUSMods project, here are some takeaways and suggestions that are applicable to TEAMMATES:

- Open up the Slack channels. Though TEAMMATES does use a communication channel outside of GitHub, it is primarily used by current CS3282 students. Even then, project-specific channels are made private. This restricts other interested contributors from being informed about what's happening and the reasons for certain decisions. For example, [this issue](https://github.com/TEAMMATES/teammates-ops/issues/3) does not provide any useful information (maybe it's supposed to be that way, but the point still holds). 

  TEAMMATES should invite potential contributors to join the Slack workspace, unless there are some external factors behind the current decision (like requiring a paid Slack plan in case the number of messages increases by a large amount; this is unlikely, but something to consider). 

- Though TEAMMATES has good documentation as compared to many other open source projects, it can use a couple of minor updates:
  - Explain what files are in which directory in the contributors orientation guide, similar to NUSMods' subprojects. This will prove useful to newcomers especially now, since we are in the process of migration. A new contributor faced a [similar issue](https://github.com/TEAMMATES/teammates/pull/9602#pullrequestreview-218052367) which could have been prevented by stating that the frontend of the project has been moved to the `src/web` folder and the legacy files are meant to be deprecated.
  - The code documentation is decent, but can still be improved in terms of the covered classes and functions, as well as the level of detail (especially if there is something important that needs to be noted). This is not critical, and will require a considerable amount of effort too.

- In terms of code style, TEAMMATES can use absolute paths for TypeScript. Since using Webpack like NUSMods may be too heavy, alternatives like [modifying the `tsconfig`](https://medium.com/@adrianfaciu/use-absolute-paths-for-module-imports-6e5ee9e94161) can be considered instead.

