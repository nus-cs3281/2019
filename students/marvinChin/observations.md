# [Docusaurus](https://github.com/facebook/Docusaurus)

# Project Documents
#### Workflow
- [Project Readme](https://github.com/facebook/Docusaurus/blob/master/README.md)
- [Contributing Guide](https://github.com/facebook/Docusaurus/blob/master/CONTRIBUTING.md)
#### Product Roadmap
- [Docusaurus V2 RFC](https://github.com/facebook/Docusaurus/issues/789)
- [Docusaurus V2 Design Document](https://docs.google.com/document/u/0/)
#### Product
- [User Documentation](https://docusaurus.io/docs/en/installation)

# My Contributions
- [fix: missing default value for grid block content objects #1186](https://github.com/facebook/Docusaurus/pull/1186)
- [docs: add missing trailing slash to sample site config base url #1190](https://github.com/facebook/Docusaurus/pull/1190)
- [fix: wrong padding for single row mobile nav #1191](https://github.com/facebook/Docusaurus/pull/1191)
- [fix: docs asset links should follow specified docsUrl #1204](https://github.com/facebook/Docusaurus/pull/1204)
- [Use clean url for og:url when cleanUrl is true #1242](https://github.com/facebook/Docusaurus/pull/1242)

# What I Learnt
#### Workflow
- How to get onboarded to a project asynchronously, without having to communicate directly with the maintainers of the project. This was possible because:
    - **Clear contributing guidelines** makes it easy to figure out **how to contribute effectively** to the project.
    - **Clean project structure and code** makes it easy to figure out **how the product works**, and by extension **how to work on the codebase**.
- How to easily find issues to work on for OSS projects. This was possible because:
    - **Good and concise tags** that describe the issue (e.g. `bug` or `feature request`) which helps contributors to quickly identify the issues that interest them.
    - Maintainers provide an **estimated difficulty level**, so that contributors can determine whether the issue is likely to be workable for them based on their own familarity with the codebase.
    - Intentionally creating/leaving a [trivial issue](https://github.com/facebook/Docusaurus/issues/1080) for new contributors to work on helps to encourage potential new contributors to get started with the codebase without being too intimidated by harder issues.
- Communication between users, contributors and maintainers can remain straightforward and effective even if it is completely asynchronous. This is helped by using the appropriate medium for different types of communication:
    - **Persistent and crowdsourced issues** (e.g. feature requests, bug reports) are communicated via the **GitHub issue tracker**. This is an effective way for users/contributors to share information that may be useful to the rest of the community.
    - More **general, maintainer driven ideas** (e.g. product roadmap and design documents) are communicated via more centralized mediums such as **Google Docs, Markdown documents on GitHub, and the project blog** which is more suitable for longer documents.
    - More **short-lived conversations**, where information shared is more self-contained and does not need to be shared with the broader pool of users or contributors (e.g. help getting started) can be held in the **Discord channel**.
#### Development
- How to organize code in a way that is easily readable and extensible:
    - The Docusaurus codebase makes **heavy use of abstractions**. Most components, methods, and even files are relatively short. By **containing only as much logic in each abstraction as necessary**, the codebase becomes significantly **easier to read and reason about**.
    - Good, descriptive variable names are essential for understandable code. Some useful conventions: method names should **start with a verb**, and variable names should be nouns that describe the **content and intended use** of the variable.
    - Opt for **readability over conciseness**, especially for complex boolean statements (e.g. `!link.languages && !link.search` is harder to understand than `!(link.languages || link.search)`).
    - Sometimes, using mutatable variables (sparingly!) can help improve code readability, and avoid having too many variable names that need to be kept track of.
- Using good tooling can improve developer productivity:
    - Using a **good code formatter** (Prettier in this case) allowed the project to retain a consistent coding style despite having multiple authors working on it. Contributors did not have to worry about how the code was formatted, which reduced a lot of friction in the review process, as well as cognitive overhead when writing the code.
    - Using a test framework that supports **component-level snapshot testing** (Jest) allowed tests to be easier to write and maintain by reducing the scope of each individual test case.

#### Product
- A clear product vision helps to align the expectations and goals of both users and developers (though this may sound trivial, I feel that these traits are crucial to building and growing a strong community surrounding the project and allow it to grow):
    - The **clearly stated aim** for Docusarus to facilitate "easily building, deploying, and maintaining open source project websites" - which gives users and developers a **clear idea of what to expect from the product**. This is not only useful for the core maintainers to decide what features to work on along with their priority, but also for other contributors to feel confident in the long-term vision of the product they are working on.
    - Similarly, **offering a product roadmap** gives users and contributors a **sense of how the project will evolve**. This can help get buy-in from users by helping them to decide if it is the right project for their use case. For developers, this can give them a better idea of what kind of work they might be doing should they decide to be a long-term contributor to the project.


# Suggestions for Internal Project
- **Write (good!) contributing resources**
    - As the MarkBind team changes with every CS3281/2 batch, it is essential for the project to be accessible to new contributors. It would be more productive if each new batch is able to onboard themselves to the project with minimal guidance from senior developers.
    - Furthermore, if MarkBind is to grow as an OSS project, it would be necessary for external contributors to get involved. Without contributing documentation, external contributors may be less willing to get started working on the project.
- **Improve abstractions in the codebase**
    - The current codebase has several *massive* files and methods (e.g. `Site.js` and `Page.js`) and some really complex methods (e.g. `parser.js`) that are difficult to understand, and even harder to maintain or extend.
    - Breaking these down into more layers of abstraction can help improve readability, as well as code reuse.
- **Offer a more real-time form of communication**
    - At the moment, all communication with external parties (both contributors and users) is done via either email or the GitHub issue tracker. While this is good for slower-paced discussions, it is not very effective for quick conversations.
    - Having an alternate channel for such discussions (e.g. Discord, IRC, Telegram) could be useful for new users or contributors to get quick responses for the issues they face. The quicker responses via these channels might be important to drive adoption of MarkBind in an already crowded space.
- **Have a clearly stated product vision and roadmap**
    - Though there is a product vision that is shared internally (to be the best site for documentation websites), this vision is not shared with the public.
    - By clearly stating the product vision, external users and contributors are able to more clearly assess if the project suits their use case, and help generate buy-in from these parties.
- **Better Tooling**
    - Adopting a code formatter could improve developer productivity by standardizing the formatting of the codebase. Though there are [challenges](https://github.com/MarkBind/markbind/pull/758) in adopting a formatting tool in an existing project, I feel that finding the right tool/configurations for this is worth the initial effort and inconvenience getting used to a different formatting style as it *really* helps improve consistency and productivity - especially as the size of the team grows.
    - Using Jest's snapshot testing to test the HTML output from individual Markdown snippets can allow user-facing features (e.g. `include`) to be easily unit tested without having to rely solely on system tests. This can be helpful in identifying regressions more effectively than [examining potentially large diffs](https://github.com/MarkBind/markbind/issues/761#issuecomment-472759620) generated by our existing system tests.
- **Use a Javascript UI library**
    - At the moment, large parts of the site's HTML is generated by a combination of EJS templates, a Vue component library, and *plenty* of raw string handling.
    - This can be rather unwieldy at times, and having several different entry points to changing the output of the site makes the rendering process unnecessarily complex and difficult to understand.
    - We might want to consider how this can be avoided by using a single Javascript UI library (e.g. Vue or React) to handle *all* of the HTML generation. This would allow us to use one consistent layer of abstraction to deal with all HTML generation logic.
    - This would require an overhaul of large portions of the existing logic - which might not be the best idea. Perhaps this is something that might be considered for future iterations of MarkBind.

# Suggestions for External Project
- **Use System Tests**:
    - At the moment, automated tests for the project are limited to unit tests. Most system level tests (e.g. how the entire site looks) requires manual testing.
    - Using automated system tests to create a snapshot of a sample test site (similar to MarkBind) could help to automate this process and prevent regressions that are not detectable by the unit tests.