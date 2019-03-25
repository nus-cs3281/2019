## External Project: Rocket.Chat iOS

### Contributions: 

1. [[IMPROVEMENT] Add editing changed handler to UITextField in connect screen](https://github.com/RocketChat/Rocket.Chat.iOS/pull/2494)
2. [[NEW FEATURE] Support in-app announcements](https://github.com/RocketChat/Rocket.Chat.iOS/pull/2514)
3. [[IMPROVEMENT] Auto suggesting slash commands even when not first character](https://github.com/RocketChat/Rocket.Chat.iOS/pull/2599)

### Introduction

[Rocket.Chat](https://rocket.chat/) is a free, open-sourced team communication application that allows teams and individuals to communicate and collaborate using text chats, video and audio calls, and also supports screen sharing. It is an application supported on multiple platforms, including Windows, MacOS, Linux, Android and iOS. I chose to work on the iOS application for my external project as I was intrigued by the many features this application boasts and I also hoped to be able to learn a couple of new things along the way. Over the course of the semester, I was able to contribute improvements in 2 areas, and also add a new feature to the application.

### Workflow

Rocket.Chat provides a brief [contributor's guide](https://github.com/RocketChat/Rocket.Chat.iOS/blob/develop/CONTRIBUTING.md) for people who are interested in contributing to the project. It is a largely a pretty standard workflow, where contributors simply fork and clone the project, work on the changes on a new branch, then open a pull request when ready. They have naming rules for issues, PRs and branches which help keep things organised, and some special branch names also help to automatically skip CI builds.

### Things I learned

#### 1. Documentation is helpful and important

During the first few days of working on Rocket.Chat, I found myself lost in the thousands of lines of code, not knowing where to begin to look for the source of the bug. Usually when this is the case, we would go and look for any sort of documentation or developer guide to help us understand the code faster and to know more details, for example which classes are responsible for which features, etc. However, Rocket.Chat does not have any such documentation for its iOS application, but only has a small contirbutor's guide which does not have any details about the codebase itself.

Much of my time was actually spent trying to read and understand the code, rather than to think about and write out the solution for the problem I was trying to fix. I feel that this is a rather inefficient way of working, especially in a big project like Rocket.Chat, it would be better if there was some sort of documented guide for developers so that the time spent on trying to understand the codebase is minimised. 

The saving grace was that the codebase was actually relatively neat and readable.

#### 2. In an open-source project, an active and helpful community is important.

Continuing from my first point above, while documentation was lacking, the developer community in Rocket.Chat is strong and everyone is very helpful. From the maintainers to the senior contributors and the newcomers, it seemed like everyone was friendly and eager to help each other out, and everyone's queries are all promptly answered on both the PR thread, issue threads, and also a developer channel within the application itself! (it is a chat app that has a public server for all to join).

I was actually stuck on an [issue]() for quite some time, initially relunctant to ask for help (because it was a pretty trivial problem!). But once I did reach out on the PR thread, I had a couple of replies within the next day or two, and was able to open a PR within the next week. 

#### 3. While it's good to be nice, code reviews must be taken seriously.

In all my contributions to Rocket.Chat, I find that the code reviews by the maintainers were all very thorough and detailed, and they always look to test and make sure the solution is working before it can be merged. They also require that the CI tests be passing before PRs are allowed to be merged. This is how they slowly build up a very clean and readable codebase, and it makes things easier for future developers as the process learning the codebase becomes less of a chore. I found myself slowly incorporating the practice of thorough and detailed code reviews into PowerPointLabs as well, as I realised the many benefits of not only merging working code, but also good quality code. 

### Comparisons to PowerPointLabs

PowerPointLabs can benefit from better community engagement and involvement, for both users and contributors. Possible ways are perhaps a public Slack channel where users and contributors are free to join and everyone can ask for any help and whoever is able to answer can help to solve the problem. Currently, we are handling user feedback and bug reports via email, which is not as personal and due to a one-to-one correspondence with the user, it might result in repeated work for us maintainers to give the same answer to the same question from different people. Having such a public space for direct messages can also make the exchange between users feel more personal and human.

In PowerPointLabs, while we do not have the best documentation, we do have some basic technical guides targeted at developers and contributors that can help with some of the technical issues that may arise during development in the project. In this instance, I think that Rocket.Chat can probably benefit from some sort of technical documentation to aid developers in writing code for the application, given the fact that is it actually a pretty large application.
