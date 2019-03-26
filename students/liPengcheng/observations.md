**Project**: [Oppia](https://github.com/oppia/oppia)

**Contributions**

- [Fix backend test coverage for core.controllers.collection_viewer](https://github.com/oppia/oppia/pull/6427)
- [Fix backend test coverage for core.controllers.collection_editor](https://github.com/oppia/oppia/pull/6462)

**Link to getting started with Oppia**

- [Wiki list of entire documentation and help](https://github.com/oppia/oppia/wiki)
- [Contributing to Oppia](https://github.com/oppia/oppia/wiki/Contributing-code-to-Oppia#setting-things-up)

**Observations about the project**

**About the Project** - Oppia is an online learning tool that enables anyone to easily create and share interactive activities (called `explorations`). These activities simulate a one-on-one conversation with a tutor, making it possible for students to learn by doing while getting feedback.

I chose this project as I believe a tool to help with learning is very important. Also, Oppia uses a framework which I am already comfortable with. Oppia is built with Google App Engine and it uses Python as the backend and AngularJS as the frontend framework. This is fairly similar to Teammates which makes a good platform to apply the things I learnt about Angular and also understand how to write Python backend code.

#### Key takeaways:

While I learned about the general framework of using AngularJS and Python, I also learned about integrating testing tools offered by AngularJS such as Jasmine and Karma.

**1. High Testable Code** - I recognize the importance of having extensive tests ranging from backend, frontend to E2E test. It is important to cover all the test cases in order to ensure that the application does not fail in any way.

**2. Interaction with fellow developers** - Oppia uses `Glitter` to welcome, communicate and disseminate any important announcements to the development of the application. I feel that it is a great way to understand how senior developers think and challenges they faced.

**Improvements for Oppia**

**1.** Since it is a fairly large codebase, it will be good if the project can support or promote an IDE to help with development, similar to what TEAMMATES has done. Currently you can only run the virtual environment server in terminal.

**2.** It is good that there is a documentation template for each component in order to standardize. However, only the high level documentation is completed and it relies strongly on contributers to help with the documentation of smaller components which has no progress for months. Hence, basic documentation of each component could be completed to help contributors in the process.

**3.** There is no default data in local server which helps developers to understand the web application better. This practice is followed in TEAMMATES and it will be a good addition to the Oppia project.

**Suggestions for TEAMMATES**

**1.** TEAMMATES could consider incorporating a channel and survey system in onboarding new developers. Oppia requires new developers to fill up a survey so that its team can allocate the right project for each developer depending on the strength, availability and goal of the developer.

**2.** Another area that TEAMMATES can work on is to allocate mini projects to contributors who have made a certain number of contributions. Oppia invites developers to be collaborators after 2 merged PRs to help out with more in-depth projects and dicussions.

**3.** In terms of testing, Oppia is very driven by codecov report and aims to get 100% coverage for all tests so they have open PRs for anyone to work on any tests to help to improve the coverage. Since TEAMMATES also aim to achieve high coverage, there can be issues opened for anyone to work on improving tests cases as well.

**4.** Oppia made users to automatically check all styling before a successful push can be made to the repository. I think this is applicable to TEAMMATES to help to reduce the check style fails.
