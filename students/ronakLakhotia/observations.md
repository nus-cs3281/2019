## **Project**: [Exercism](https://github.com/exercism/java)

**Contributions**

- [Update Error handling mechanism for existing exercise](https://github.com/exercism/java/pull/1635)
- [Update Tests for existing exercise](https://github.com/exercism/java/pull/1639)

**Links to getting started with Exercism**

- [Finding your way](https://github.com/exercism/docs/blob/master/finding-your-way.md)
- [Contributing to language tracks](https://github.com/exercism/docs/blob/master/contributing-to-language-tracks/README.md)

**Observations about the project**

**About the Project** - Exercism is an online platform designed to help you improve your coding skills through practice and mentorship. Exercism provides you with thousands of exercises spread across numerous language tracks. Once you start a language track you are presented with a core set of exercises to complete. Each one is a fun and interesting challenge designed to teach you a little more about the features of a language.

**1.** It provides you with thousands of exercises spread across numerous language tracks. I decided on contributing to Exercism because of the **number of language tracks** that a developer can choose from. Since I am most comfortable with Java, I made pull requests to the [Java Learning Track](https://github.com/exercism/java).
One can find other languages like C++, Python, JavaScript and many more.

**2.** Exercism uses **tools** like [Exalysis](https://github.com/exercism/exalysis) that automatically runs the tests on a solution and makes some helpful suggestions based on static analysis of the code for common errors and patterns.
They even have a [Command Line Tool](https://github.com/exercism/cli) for interacting with the [website](https://exercism.io/) from the local environment.

**3.** The project **workflow is smooth** in general. Mentors are always ready to help new developers during the initial stages. The exercism community is active and there is an online chat room too where mentors and developers can discuss their ideas. For instance, while working on one of the PRs, there were a couple of mentors who suggested changes to my implementation. They did so in a nice and helpful manner which I feel is important for attracting new contributors to an open-source project.

**Key Takeaways from this Project**

**1. Suggesting Alternative Viewpoints -** An important thing I learned while contributing was to not be reluctant in suggesting alternative ways for a particular implementation.
It is a good practice to discuss ideas with the mentors and eventually settle on the best path.

**2. High Quality Code -** Writing code that is readable to other developers is very important. In fact documentation in the form of comments should be minimal. Most Exercism projects encourage contributors to write code that is readable and does not need the aid of comments.

**3. Interaction with fellow developers -** Exercism has a dedicated communication channel that allows developers to collaborate and discuss ideas/solutions. It is a great way to network and also provides you with  an opportunity to communicate with mentors who have experience in the industry for a long time.

**Improvements for Exercism**

**1.** The documentation for Exercism could be improved. Making use of architecture diagrams or perhaps other visual aids should be included to help new developers get used to the codebase.

**2.** Perhaps the issues could be labelled to help newcomers. This practice is followed in TEAMMATES and can be a good addition to the Exercism project.

## **Project**: [JabRef](https://github.com/JabRef/jabref/)

**Contributions**

- [Added additional key bindings](https://github.com/JabRef/jabref/pull/4732)
- [Co-Authored a PR](https://github.com/JabRef/jabref/pull/4727)
- [Added integrity checks](https://github.com/JabRef/jabref/pull/4642)

**Links to getting started**

- [Get an idea about the project from the official website](https://www.jabref.org/#jabref)
- [FAQ on Contributing](http://help.jabref.org/en/FAQcontributing)

**Observations about the project**

**About the Project** - JabRef is a cross-platform citation and reference management tool. It helps you collect and organize sources, find the paper you need and discover the latest research. 

**1.** For every change made, updating documents is a must and it is a part of the PR checklist. This practice must be followed before a PR gets merged. It enforces good standards of documentation to be followed consistently.

**2.** The review process requires at least two senior devs to approve your PR before it gets merged. This means the code reviews will be thorough as was the case when I submitted PRs to the project.

**3.** The issues have proper labelling, each of them categorize according to the description and which part of the application it is relevant to. This is very important to allow new contributors to get used to the environment and make them feel at ease.

**4.** The project uses tools like Codacy and [DEP](https://github.com/z0al/dep). Codacy automates the review process and eases development workflow. It has been made a part of the CI workflow where if your PR fails certain thresholds of code quality, the build will fail. DEP is a bot that checks for PR dependencies and tells the developer if other issues need to be resolved before the current PR can be merged. This is a good way to manage a particularly large project.

**Key Takeaways from this Project**

**1. Emphasis on Documentation** - An important takeaway was that, JabRef encourages contributors to keep updating the documentation with every PR, which is quite interesting as I have not come across his practice in other projects. Such practices can be enforced by other OSS projects too.

**2. Asking for help** - The JabRef community is big and help is readily available. Contributors are encouraged to discuss ideas and methods of implementation. They even have a [gitter channel](https://gitter.im/JabRef/jabref) to welcome new contributors where once can post queries.

**Improvements for JabRef**

**1.** JabRef can perhaps can improve their documentation of setting up the project. It will help the newcomers ease into the new environment. Currently, it seems a bit convoluted. Perhaps, having a cleaner workflow will make it easier for new contributors to set up the project. Another possible addition could be to use video tutorials to make it easier for contributors to follow the set-up process.

## **Project**: [apps-android-commons](https://github.com/commons-app/apps-android-commons/)

**Contributions**

- [Fixed lint errors](https://github.com/commons-app/apps-android-commons/pull/2359)

**Links to getting started**

- [Contribution Documentation](https://github.com/commons-app/apps-android-commons/wiki#contributor-documentation)
- [App functionality](https://github.com/commons-app/apps-android-commons/wiki/App-functionality)
                         
**Observations about the project**

**About the Project** - The Wikimedia Commons Android app allows users to upload pictures from their Android phone/tablet to Wikimedia Commons.

**1.** The project workflow is easy to follow and mentors are always ready to help. The senior devs guide new contributors and are patient throughout the process.

**2.** Since the project deals with a mobile application, each change made in the PR requires developers to upload screenshots. This is to ensure that no regressions have occurred due to your changes. This was unique for me because I have never worked on a Mobile application before.

**Key Takeaways from this Project**

**1. Testing your code -** Mentors emphasize on the importance of testing. Your changes should have relevant test cases before it is up for review. A lot of importance is placed on the code coverage of your PR.
   
**1. Automated review process -** The project makes use of Codacy to automate the review process in the initial stages. Metrics are set failing which the PR build will fail. I think it is a great way to enforce good engineering practices.
                                                                         
**Suggestions for TEAMMATES**

**1.** A practice that TEAMMATES could adopt from Exercism is to have a dedicated channel for new developers coming into the organization. This can really help in the on-boarding process and ease new developers into the new environment. An advantage of this is that the communications carried out in Github can be taken to slack channels where the process will be faster. It also gives new contributors an opportunity to ask clarifying questions.

**2.** Another area that TEAMMATES can work on is to grow the number of students running the organization. It might make the development process faster if more mentors are on-board to drive the project forward. The logistic constraints are understandable which is why incoming contributors must be encouraged to stick with the organization and help maintain it as the user base continues to grow. 

**3.** TEAMMATES could consider using automated tools for code review. This will help ease the workload on senior devs by pointing out common error patterns and improvements in a PR. As a side note, TEAMMATES can also start a technical blog to show potential users and developers the new changes being worked on. For instance we could mention about migrating to Angular, following a REST architecture, etc.
