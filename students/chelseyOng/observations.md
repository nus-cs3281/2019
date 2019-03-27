## **Project**: [JabRef](https://github.com/JabRef/jabref) 

JabRef is a citation and reference management tool that helps you collect and organize your research materials.

### Links
+ [Contributing guidelines](https://github.com/JabRef/jabref/blob/master/CONTRIBUTING.md)
+ [Setting up workspace](https://github.com/JabRef/jabref/wiki/Guidelines-for-setting-up-a-local-workspace)
+ [Help contents](https://help.jabref.org/en/)

### Contributions made:
+ Add a variable to track the change in preview style #4587 ([Issue](https://github.com/JabRef/jabref/issues/4580), [PR](https://github.com/JabRef/jabref/pull/4587))
+ [Enable default cursor for new entry #4604](https://github.com/JabRef/jabref/pull/4604)
+ [Fix preview style configuration #4613](https://github.com/JabRef/jabref/pull/4613)
+ [Fix: bibkey generated does not handle diacritics #4713](https://github.com/JabRef/jabref/pull/4713)

### Workflow
For each pull request made, it is required to fill in a checklist. The checklist looks for 6 points - Tests are created, manual testing is done, screenshots added if UI is to change, good git commit messages are written, documentation is updated, and the change is properly logged in the file.

I feel that this is a very good practice to remind developers to fulfil a certain criteria before requesting for reviews from the developers. This is especially useful for newcomers who are not familiar with the project's contributing workflow. In a way, this can also speed up the reviewing process as reviewers do not have to check for things that are already on the checklist so they can focus on ensuring good code is written instead. However, in JabRef, this checklist is commonly ignored and only certain bulletpoints are looked out for. I believe they can update this checklist to make it more relevant to both new and existing contributors. For example, the documentation status seems redundant as it is often expected of the PR author to update documentation when the code changes.

Issues are also organized into 3 categories, namely [JabRef UI Usability Improvements, Bugs, and JavaFX UI Rework](https://github.com/JabRef/jabref/projects). Every category has a set of issues with differing priorities. Whenever an issue is closed, an automated bot will move it into the "closed" group. This is an interesting way of tracking all issues and their assigned priority levels at a glance. As RepoSense is solely relying on the issue tracker which acts like a "noticeboard" for all the issues posted, it can become hard to handle when there are more bug reports or feature requests with the increased number of users in future. By partitioning issues into relevant categories, developers have a more efficient way of looking at a smaller pool of issues that deserve greater attention.

### Tools used
The tools used by JabRef are Codacy, Travis CI and [DEP](https://github.com/z0al/dep). CI does a good job in ensuring that the new code passes all tests, including integration and database tests. Codacy is mainly used to check for checkstyle issues. DEP is a bot that checks for PRs which rely on other PRs/issues to be merged before they can be continued. It becomes useful when many people are working on similar areas in the project at the same time. Developers become more aware that they are working in a group and close collaboration is often needed to ensure good code quality. This may be applicable to RepoSense's frontend development where many conflicts occur when new PRs are merged and this can slow down the whole contributing process and bring in unnecessary bugs in the code.

### Documentation
There is a Wiki page on JabRef that provides information about how to use JabRef and ways of contributing and developing code, such as [best code practices](https://github.com/JabRef/jabref/wiki/Code-Howtos) used by JabRef specifically. As such, new code written can fit into JabRef's context easily. This is similar to the User and Developer Guide already used in RepoSense. In future when more tools are integrated into RepoSense, notes on how tools RepoSense use can contribute to a better contribution workflow, may be written in the Developer Guide to teach new developers how to use these tools more effectively. A FAQ section can also be written in the Wiki page, especially common questions that are often asked by students who are using RepoSense. A benefit of using a wiki page instead of a markdown file for documentation, is the ease of browsing through the different sections, without having to scroll back to the top of the page to find the table of contents, as this can be quite frustrating for new users who are struggling to use RepoSense.

I had encountered some difficulties trying to set up the project, because it uses JDK8 and some deprecated libraries that cannot be resolved by IntelliJ. Since new JDK libraries are mostly used in development these days, using older libraries can slow down the setting up process and delay the time used to write actual code.  Git submodules have to be installed to use citation styles when viewing reference entries, but I feel that it is actually quite neat to be able to install additional libraries through Git without having to download another set of files during the development stage. Nevertheless, the guidelines provided by JabRef are very easy to follow along. Additional help from the JabRef community is also available through the [gitter channel](https://gitter.im/JabRef/jabref). If one prefers learning by following instructions, a video tutorial is also available. 