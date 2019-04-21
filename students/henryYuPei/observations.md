# External project: Git for Visual Studio
[link](https://github.com/github/VisualStudio)

## Online documents of project's workflow
* [Build requirements and steps](https://github.com/github/VisualStudio#build-requirements)
* [Common issues when setting up](https://github.com/github/VisualStudio#troubleshooting)
* [Contributing guide](https://github.com/github/VisualStudio/blob/master/CONTRIBUTING.md)
* [Contributor Covenant Code of Conduct](https://github.com/github/VisualStudio/blob/master/CODE_OF_CONDUCT.md)
* [Writing a good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
* [Submitting an issue](https://github.com/github/VisualStudio/blob/master/CONTRIBUTING.md#submitting-an-issue)
* [Documentation](https://github.com/github/VisualStudio/tree/master/docs)

## Things learnt from project
* Error dialogs in the application are extremely helpful in assisting new contributors in finding code related to bugs,
in a project of such a scale (estimate over 30k LoC, with many modules).
* Finding more `good first issues` might be a good way to encourage new contributors to help out.
Currently there is only 1 `good first issue` and is stale as someone asked to do the issue, but his rather old PR did not get closed after a rather long period.
[link to PR](https://github.com/github/VisualStudio/pull/1989). This made me a little reluctant to start as other issues require some amount of understanding
of a significant part of the project. It is observed that the external project does not receive new contributors often.
* Adding a label to an issue to describe the scope of the bug can be very helpful for new contributors. I had to rely solely on error dialogs, debuggers and some logging to find the cause of a bug.
* PRs that lacked description of what it fixes, how it is fixed and what tests are written are often rejected. This is important as both the contributor and the developr should
be confident of the changes being introduced.
* The project uses a `ReadyForReview` label for developers.
* The project seems to be open to adhoc documentation fixes from public contributors. [Example](https://github.com/github/VisualStudio/pull/2231)
* The project uses milestone deadlines to have certain PRs merged/reviewed/completed. However, the pattern is not clear.
* The project merges PRs that fail CI tests by their internal memebers, probably because CI tools report false positives at times.
* The project uses [projects](https://github.com/github/VisualStudio/projects) to manage issues pertaining to different aspects of project management, such as maintaining/building a feature area,
or fixing bugs and polishing the code.
* The project uses [development sprints](https://github.com/github/VisualStudio/issues/2240) to push new enhancements. The project also utilises a [bot](https://github.com/github/VisualStudio/releases)
to push new releases.

## Practices/tools of the external project that may be adoptable by NUS-OSS
* Use milestone deadlines for PRs/issues.
* Use projects to plan for longer term development.
* Use a bot to publish releases, and have development sprints (but the team is a little small for benefits).

## [Optional] Suggested areas of improvement for the external project
