### Project: [Gatsby](https://www.gatsbyjs.org/)

Gatsby is an open source framework based on React that helps developers build websites and applications faster.
- [How to Contribute](https://www.gatsbyjs.org/contributing/how-to-contribute/): Information on contributing to issues, documentation, product website, and codebase.
- [RFC Process](https://www.gatsbyjs.org/contributing/rfc-process/): Details on contributing substantial changes (using the requests for comments process).
- [Gatsby Style Guide](https://www.gatsbyjs.org/contributing/gatsby-style-guide/): Guidelines for writing documentation and tutorials.

### Contributions
- [fix(www): prevent filter accordions from disappearing on collapse](https://github.com/gatsbyjs/gatsby/pull/12727)
- [fix(gatsby-dev-cli): move package.json file check after pathToRepo handling](https://github.com/gatsbyjs/gatsby/pull/11565)
- [Issue #12517](https://github.com/gatsbyjs/gatsby/issues/12517)
- [Issue #12845](https://github.com/gatsbyjs/gatsby/issues/12845)

### What I Learnt

1. **Define and Enforce a Workflow**: Gatsby follows the standard forking workflow for bug fixes and small enhancements. More substantial changes follow the Requests for Comments process. Contributors must open a pull request that has a detailed document regarding their proposed change in a [separate repository](https://github.com/gatsbyjs/rfcs) dedicated to RFCs. Having a separate repository provides an exclusive space for more focussed discussions on new features. I could see how this process is beneficial for a large open-source project like Gatsby as it helps them to control how new features are added to the project. 
2. **Have Dedicated Code Owners**: Gatsby has 5 teams of [maintainers](https://github.com/orgs/gatsbyjs/teams/maintainers) that take ownership of different areas of the project. For example, pull requests need a review from the respective code owners. Managing a huge project like Gatsby can be quite difficult for maintainers as it has the codebase, product website, documentation, and other ecosystem features like themes and plugins. Having dedicated code owners makes it more convenient for the maintainers to handle issues and review pull requests in areas they are most experienced in.
3. **Automate Repetitive Tasks**: As it’s a popular product, Gatsby has a lot of activity in its issue tracker. Gatsby uses a [bot](https://github.com/apps/gatsbot) to automate some repetitive tasks, like labelling issues based on their content and closing issues after inactivity. Additionally, they use a [bot](https://github.com/marketplace/renovate) to update the project’s dependencies. Contributors also have have to follow specific pull request and branch naming guidelines which makes it easier for automated tasks to be run on them.
4. **Motivate your Contributors**: For an open-source project, motivating your contributors is extremely important. Gatsby has a comprehensive guide for contributors, which includes basic information on how to triage and label issues, submit pull requests, and writing good documentation. It also has an [advanced guide](https://www.gatsbyjs.org/docs/behind-the-scenes/) that explains how Gatsby works behind the scenes. The quality of the contributing guide is what motivated me to work on this project, as it showed me that the project was serious about helping its contributors. Gatsby encourages [contributions](https://www.gatsbyjs.org/contributing/where-to-participate/) other than pull requests and commits. And there’s [free swag for all contributors](https://www.gatsbyjs.org/contributing/contributor-swag/) too!
5. **Interact with your Community**: Gatsby has their own [Discord channel](https://discordapp.com/invite/br9rbUE) for providing faster support to those who need it. They also host free [pair programming sessions](https://www.gatsbyjs.org/contributing/pair-programming/) where you can work on fixing an issue with a senior developer. Interacting with your project’s open-source community is important because it provides developers with a pool of resources, which gets things done faster.

### Suggestions for MarkBind

1. **RFC Process**: Even though having a separate repository for proposing substantial code changes can be overkill, the RFC process could still be incorporated for adding new features to MarkBind.
2. **Better Bug Reports**: Require users to submit standalone MarkBind sites for reproducible test cases. Gatsby asks its users to create a new Gatsby site and add only those lines of code or plugins that cause a problem, publish the code, and link it in the bug report. This will be beneficial for MarkBind because the developers would not need to dig in through a lot of code to find the error, in addition to knowing the exact environment of the bug report.
3. **Issue Categories**: MarkBind already has issue templates, but we can take one step further and have different templates for different categories of issues like Gatsby does. For example, questions about using MarkBind and bug reports can have separate issue templates. 
4. **Comprehensive Contribution Guide**: MarkBind will definitely benefit from a dedicated guide for new contributors on its product website.
5. **Guides for Different Use Cases**: Gatsby has standalone [advanced tutorials](https://www.gatsbyjs.org/docs/advanced-tutorials/) for developing websites that have different use cases. MarkBind could have guides for developing a site that serves as a textbook, project documentation, or an eLearning resource. This will also showcase MarkBind's different features and versatility.
