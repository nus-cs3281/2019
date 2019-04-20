## **External Project:** Electron

**Links:** <br>
[Electron Development Documentations](https://electronjs.org/docs/development)

I appreciate their very structured and ordered contribution guideline, as Electron is a very big open source software. Not only that, Electron has quite cool contribution flow, going all the way from creating issue to getting your PR merged. What I observed from their process as well as how it might be applied to RepoSense are as follow:
- **Structured Issue message** <br>
This is to ensure that the issue can be triaged faster and more efficient. This goes all the way from differentiating bug issue and feature request issue, and then there is issue template that developer can follow including a checklist for developer whether they have checked for existing issue, etc. <br>
RepoSense perhaps can follow this procedure to improve issue management.
- **Semantic commit message** <br>
Electron follows [Semantic Commit Message](https://www.conventionalcommits.org/en/v1.0.0-beta.3/) to streamline release process. RepoSense can implement this alternative commit message guideline if it does not want to follow the rigorous SE-EDU as for now RepoSense does not really have any commit message guideline.
- **Semantic Prefix for PR Title** <br>
This is to ensure that the PRs are nicely organized. This enforcement is mandatory in Electron. RepoSense can learn to implement this better as PR title in RepoSense is still quite haphazard.
- **Semantic PR message** <br>
Electron's semantic PR message is not only for stylistic purpose, but it is linked to their bot automation. For example, you can include release note by adding `notes:`, which will be detected by Electron's *release note bot* and then it will process accordingly. While this may be an overkill feature, RepoSense can follow this structure if it will use automations in the build and release process in the future. The automations involving bot will be expanded below.
- **Welcome Bot** <br>
Electron has a bot that welcomes new contributor. Upon creating their first PR and merging it, they will be greeted with the bot. The bot will remind the user with all the contribution guidelines so the user can follow in closely if they have failed to read it beforehand. RepoSense can benefit from this when RepoSense is larger to remind new contributor what to do when they have submitted their PR. Also, with the welcome bot we can easily differentiate who is a new developer to RepoSense and who is not.
- **Clerk Release Note Bot** <br>
The bot checks for `notes:` prefix in PR message and update the release note accordingly. This is according to the idea that `commit -m` is for maintainers while `notes:` is for users. Although this bot is proprietarily developed by Electron team, RepoSense might be able to find third party alternative if RepoSense want to implement this feature in the release cycle.
- **Automatic backporting** <br>
As Electron has multiple version releases which are hosted in separate branch, a change made to latest release might need to be propagated to the previous release, essentially backporting it. This is accomplished also by automatic bot that create auto PR to previous version branch by tagging the PR with specific tag. While RepoSense currently does not have multiple version release, this idea might be beneficial for RepoSense to explore in the future.

I also appreciate that despite being a large open source software, their most active developers are very active, responsive, and helpful in providing assistance and reviewing my code. While this is something that we may already know intuitively, perhaps from this we can be reminded again to be helpful and responsive to foster a good Open Source community.

## **External Project:** NUSMods R

**Links:** <br>
[Contribution Guide](https://github.com/nusmodifications/nusmods/blob/master/CONTRIBUTING.md)

NUSMods has its own development chat channel via Telegram. Personally I think Telegram is not the best medium as it is more of a group chat where it is very easy for a discussion to go out of control and people that is not involved will not get what is actually being discussed. I found that NUSMods Telegram group is more of a group chat for the core developers and the contributors are mostly there just watching them discussing. It will be on rarer opportunity such as feature request or asking for guide from the core developers will the contributors be active in the group. I found that Slack which is already being employed by RepoSense to be more appropriate, despite RepoSense slack is not as lively as NUSMods group.

Nevertheless I appreciate NUSMods core developers openness and willingness to help. They are quick to respond and give advices, and the fact that they invite all contributors to the group and we can see all the chats there signifies those. They are also quick to reply and do not hesitate to help, signifies by my discussion with one of the core developers when I found some problem in my PR.

## **External Project:** nsfwjs

**Links:** <br>
[All Contributor Guideline (used by nsfwjs)](https://github.com/all-contributors/all-contributors)

One noteworthy observation from this project is that they follow All Contributor Guideline (link above). They acknowledge any contributors contributing in any aspects such as UI, documentation, etc. I find this to be very encouraging, especially for new open source developers and this can motivate and encourage them. I find that this will create a very warm and hospitable open source community. Perhaps RepoSense can follow this guideline or modify it to fit its own purpose to enhance current contribution acknowledgement.