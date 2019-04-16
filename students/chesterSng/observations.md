## External Project: Habitica
[Habitica](https://habitica.com/) is a an open-source, online task management application. Instead of the usual way of task management, Habitica takes it a step further by gamifying it. It turns your life into a role-playing game where you complete real life tasks for experience and gold, which can gain you better equipments to pimp your character.

### Pull Requests Merged
1. I fixed a bug where additional unusable options were displayed for certain items. [PR #10965](https://github.com/HabitRPG/habitica/pull/10965)
2. I enabled usernames to be searchable in one of the pages and added test cases. [PR #10980](https://github.com/HabitRPG/habitica/pull/10980)
3. I changed the login page to display more informative messages and added test cases. [PR #11078](https://github.com/HabitRPG/habitica/pull/11078)

### Workflow
The workflow of the project is documented [here](https://habitica.fandom.com/wiki/Using_Your_Local_Install_to_Modify_Habitica%27s_Website_and_API). It is vastly similar to PowerPointLabs, where contributors fork, create a new branch on their own repo, push changes to the branch and make a pull request. One difference is that there are no conventions to follow in Habitica in the naming of the branches and pull requests.

### Takeaways from the External Project 
Habitica has been a pleasure to contribute to because of various reasons. 

The main reason being their documentation is **clear and easy to read**. Habitica has its own wiki page that contains a lot of information about the application itself. Their [setting up guide](https://habitica.fandom.com/wiki/Setting_up_Habitica_Locally) and [instructions for contributors](https://habitica.fandom.com/wiki/Using_Your_Local_Install_to_Modify_Habitica%27s_Website_and_API) are also on the same wiki, giving a native feel to their documentation. 

Fun Fact: Contributors on Habitica are not called "contributors", they are called **Blacksmiths**.

 ##### Habitica shows Blacksmiths what they can contribute to on their [Guidance For Blacksmiths](https://habitica.fandom.com/wiki/Guidance_for_Blacksmiths).

On the same page, you can find that Habitica also introduces the workflow of the project. Some FAQs like where to add images, where to add translatable strings are on the same page. Also, even though MongoDB might be widely used, Habitica also has a small section to teach Blacksmiths how to modify the database so that they are able to test their changes. 

For someone like me who only knew MongoDB is a great database system and not know how to use it, their instructions really helped me in my contributing process. 

##### Blacksmiths are awarded Contributor Tiers

Habitica shows their appreciation for Blacksmiths by awarding Contributor Tiers once the pull request gets merged. For example, you can see in my [first pull request](https://github.com/HabitRPG/habitica/pull/10965), I was awarded the first contributor tier. In game, this achievement comes as a [badge](https://imgur.com/a/MmMJi3L) viewable in your own profile. Contributing more or longer pull requests will increase the contributor tier accordingly. Here in my [third pull request](https://github.com/HabitRPG/habitica/pull/11078), I was award the second tier. 

You can see why users of Habitica will be willing to contribute to Habitica: because Habitica gamifies the contributing as well! If you are contributing artwork or a sound piece, you will be  awarded a different [contributor title](https://habitica.fandom.com/wiki/Contributor_Titles) as well. 

##### Help is always available for Blacksmiths

Habitica has a [Guild](https://habitica.fandom.com/wiki/Guilds) set up for Aspiring Blacksmiths. Blacksmiths that have difficulty in solving the issue can post their questions on the chat where other blacksmiths or administrators will readily help and give suggestions.

### Practices/Tools that can be adopted by PowerPointLabs

##### Call/Recognition for Contributors

There are a lot of contributors for Habitica and I believe most of them are using the Habitica application themselves (since you are able to get achievements by contributing). One possible way we can more contributors for PowerPointLabs is to advertise that help is welcomed on our [website](https://www.comp.nus.edu.sg/~pptlabs/). 

In addition to that, we can have some sort of recognition for contributors. For example, having a list of names of past contributors on the github page. For example in [NUSMods](https://github.com/nusmodifications/nusmods), there is a list of contributors and their github profile pictures on their first page.

##### Continuous Integration

Habitica has a lot of tests (runs for 18mins in asynchronously, total time 45mins). This is the [Travis build](https://travis-ci.org/HabitRPG/habitica/builds/484940723?utm_source=github_status&utm_medium=notification) on my first PR. 

Continuous integration will help to keep the application away from regression. Currently, there is no easy way for PowerPointLabs to implement Continuous Integration (due to need of needing PowerPoint installed). 

As a result, extensive testing needs to be done on pull requests by reviewers manually so that the new changes will work on PowerPoint 2010, 2013 and 2016. At the same time, this is not efficient as it requires the reviewer to manually run the functional and unit tests.

##### Documentation

In comparison to the documentation in Habitica, the documentation in PowerPointLabs seems to fall short in being organised. For example, the [contributing guide](https://github.com/PowerPointLabs/PowerPointLabs/blob/master/.github/CONTRIBUTING.md) contains information about submitting an issue to the release strategy of the project. 

Althought it is very informative, perhaps we can keep the contributing guide focused and also contain relevant contributing information from the [newcomer guide](https://github.com/PowerPointLabs/PowerPointLabs/blob/master/doc/NewcomerGuide.md). 

Also, in Habitica, the documents links to each other logically. Once an interested contributor opens up the [Guidance for Blacksmiths](https://habitica.fandom.com/wiki/Guidance_for_Blacksmiths), they are provided links to the [Setting Up Guide](https://habitica.fandom.com/wiki/Guidance_for_Blacksmiths) and [Contributing Guide](https://habitica.fandom.com/wiki/Using_Your_Local_Install_to_Modify_Habitica%27s_Website_and_API).

We can also try to make PowerPointLabs guides link to each other logically also. For example, I had problems setting up the PowerPointLabs development environent on Visual Studio. However, the solution can only be found in [Common Traps](https://github.com/PowerPointLabs/PowerPointLabs/blob/dev-release/doc/CommonTraps.md), instead of the [setting up guide](https://github.com/PowerPointLabs/PowerPointLabs/blob/master/doc/ProjectSetUp.md).