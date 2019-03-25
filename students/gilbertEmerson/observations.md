**Electron**

[Electron Development Documentations](https://electronjs.org/docs/development)

I appreciate their very structured and ordered contribution guideline, as Electron is a very big open source software. Not only that, Electron has quite cool contribution flow, going all the way from creating issue to getting your PR merged. What I observed from their process as well as how it might be applied to RepoSense are as follow:
- Structured Issue message. This is to ensure that the issue can be triaged faster and more efficient.
- Specific PR title formatting. This is to ensure that the PRs are nicely organized. RepoSense is still weak in this aspect as PR title is still quite haphazard.
- Specific branch naming, although this is already implemented by NUS-OSS, RepoSense has not really enforced this aspect
- Semantic commit message, although SE-EDU standard is still better. RepoSense currently employs squashed PR but this aspect may be followed.
- Structured PR message which although may not be on same standard with SE-EDU, it is full of semantic prefixes that is linked to bot automation. For example, you can include release note by adding `notes:`, which will be detected by Electron's release note bot and then it will process accordingly. RepoSense can follow this structure if it will use automations in the build and release process which will be listed below.
- Welcome Bot that welcomes new contributor. New contributor upon creating their first PR and merging it will be greeted with the bot, which will remind the user with all the contribution guidelines so the user can follow in closely if they have failed to read it beforehand. RepoSense can benefit from this when RepoSense is larger to remind new contributor what to do when they have submitted their PR.
- Clerk Release Note Bot that checks for `notes:` in PR message and update the release note accordingly. This is according to the idea that `commit -m` is for maintainers while `notes:` is for users. Although this bot is proprietarily developed by Electron team, RepoSense might be able to find third party alternative if RepoSense want to implement this feature in the release cycle.
- As Electron has multiple version release which is hosted in separate branch, a change made to latest release might need to be propagated to the previous release, essentially backporting it. This is accomplished also by automatic bot that create auto PR to previous version branch by tagging the PR with specific tag. While RepoSense currently does not have multiple version release, this idea might be beneficial for RepoSense to explore in the future.

I also appreciate that despite being a large open source software, their most active developers are very active, responsive, and helpful in providing assistance and reviewing my code. While this is something that we may already know intuitively, perhaps from this we can be reminded again to be helpful and responsive to foster a good Open Source community.

