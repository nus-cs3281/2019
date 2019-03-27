## Project: [NUSMods](https://github.com/nusmodifications/nusmods/)

NUSMods is an unofficial module planning platform for National University of Singapore (NUS), and is practically used by all NUS students. Currently, it offers a semester timetable planner, module information bank, a course module planner, and a venue locator and availability checker.

**My Contributions:**
- Pull Requests:
	- [Highlight search period in Venues page](https://github.com/nusmodifications/nusmods/pull/1583)
	- [Clean up cyclic references](https://github.com/nusmodifications/nusmods/pull/1636)
- Reported Issues:
	- [Highlighted search period doesn't match with search options in Venues page](https://github.com/nusmodifications/nusmods/issues/1647)
	- [Footer overlaps with side navbar](https://github.com/nusmodifications/nusmods/issues/1646)

### NUSMods Project Guide

Here is an overview of the parts of the NUSMods project guide.

- The project README links to the 5 subprojects that make up the NUSMods repository. Each of these **subprojects have their own README** (with varying levels of completeness) that highlights what the subproject is about, the processes involved, and how to get started with contributing to it.

- The document also provides links to the NUSMods communication channels, the main one being Telegram. The community is active on Telegram and have **open discussions** about the project direction and design choices, apart from providing updates about new features.

- The Contributing section has the typical elements: Code of Conduct, Setting up Guide, Development Workflow. The details provided are comprehensive, yet to-the-point.
	- The project is easy to setup as subproject-specific details are provided and no project configuration or external tools (apart from standard ones like Node and Yarn) are _required_.
	- In order to fix an issue, it is recommended to state your interest in taking up the issue. This is to prevent other contributors from working on the same issue. The documentation also specifically states that if you don't follow up on it for **more than two weeks**, others can take up the issue.

### Comparison with TEAMMATES process

This section provides more specific details about the NUSMods process and practices, by comparing it with the one used by TEAMMATES.

#### Differences:

1. **Open Communication Channels**: NUSMods uses **Telegram and the GitHub issue tracker** as their primary communication channels. Uncertain features are discussed in depth in the corresponding GitHub issue so that potential contributors have an idea of how to go about resolving the issue. The Telegram group is used for requesting for help with small problems, informing members about minor updates, and some review requests.  

1. **Deploys Previews**: Netlify is part of the CI checks in pull requests (PRs) to NUSMods. Hence, each PR comes with a deployed website preview with the changes made. This allows reviewers and contributors to see the bug fix or feature in action, without needing to locally deploy the changes made in the PR.

1. **Uses Absolute Import Paths**: NUSMods uses Webpack to resolve most TypeScript import paths to absolute path, instead of relative paths like the ones in TEAMMATES.

1. **Automates Dependency Management**: NUSMods uses the [Renovate](https://github.com/marketplace/renovate) bot to automate management of its npm package dependencies. It creates new PRs when a new version of a project dependency is released. TEAMMATES doesn't have any such process. In fact, it is done manually and only on a need to basis- when a released version has a new feature or introduces several big changes, for example.  

1. **Few Active Contributors**: NUSMods only a **handful number of active contributors** since it has a smaller target audience, i.e., NUS students.  In contrast, TEAMMATES regularly gets contributors who generally fix a couple of issues. In addition, there are dedicated groups of contributors who work on subprojects, owing to CS3282.

1. **Simpler Labelling Process**: As a result of the previous point, NUSMods does not extensively use labels for PRs (like `s.toReview`, `s.finalReview`) unlike TEAMMATES which has an extensive labelling system. Since NUSMods only have a couple of project maintainers, an extensive labelling system may be overkill too.

#### Similarities:

1. **Uses Issue Templates**: Like TEAMMATES, NUSMods has GitHub issue templates for reporting bugs and requesting features. This helps standardise issue formats and also guides the authors in terms of what  information needs to be provided to make the issue complete. The NUSMods templates do feel better since they have pseudo examples that can be modified, and they specify exactly what information is to be provided in the issue description, without the template feeling too cluttered.

1. **Uses Forking Workflow**: Both projects use the forking workflow with regards to making contributions. Though maintainers have push access to the repository, they do not push directly to the `master` branch. Their contributions are still subjected to the same review process as others.

### Suggestions for TEAMMATES

After my experience contributing to the NUSMods project, here are some takeaways and suggestions that are applicable to TEAMMATES:

1. **Communication Channels**: Though TEAMMATES does use a communication channel outside of GitHub, it is primarily used by current CS3282 students. Even then, the subproject-specific channels are made private. This restricts other interested contributors from being informed about what's happening and seeing the reasoning behind certain decisions (which can be a learning opportunity). For example, [this issue](https://github.com/TEAMMATES/teammates-ops/issues/3) does not provide any useful information (maybe it's supposed to be that way, but this point still holds).

  TEAMMATES should invite potential contributors to join the Slack workspace, unless there are some external factors behind the current decision to make it selective (like requiring a paid Slack plan in case the number of messages increases by a large amount; this is unlikely, but something to consider).

1. **Documentation** Though TEAMMATES has good documentation as compared to many other open source projects, it can use a couple of minor updates:
  - **File structure**: Explain what files are in which directory in the contributors orientation guide, similar to NUSMods' subprojects. This will prove useful to newcomers, especially now, since we are in the process of migration. A new contributor faced a [similar issue](https://github.com/TEAMMATES/teammates/pull/9602#pullrequestreview-218052367) which could have been prevented by stating that the frontend of the project has been moved to the `src/web` folder and the legacy files are meant to be deprecated.
  - **Inactive contributors**: Indicate the amount of time that has to pass before an issue can be reassigned in case the previous assignee does not follow up (doesn't respond or did not make a PR).
  - **Code documentation**: It is decent, but can still be improved in terms of the covered classes and functions, as well as the level of detail (especially if there is something important that needs to be noted). This is not critical, and will require a considerable amount of effort too.
<br/>

1. **Absolute Imports**: In terms of code style, TEAMMATES can use absolute paths for TypeScript since it provides more information and better navigation, compared to relative paths. Since using Webpack (like NUSMods) may be too heavy, alternatives like [modifying the `tsconfig`](https://medium.com/@adrianfaciu/use-absolute-paths-for-module-imports-6e5ee9e94161) can be considered instead.
