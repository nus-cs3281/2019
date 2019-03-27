# External Project: [Netrunner](https://github.com/mtgred/netrunner)

# About the project.
Netrunner (hosted on [jinteki.net](https://www.jinteki.net/)) is the digital platform to play the card game [Android: Netrunner](https://www.fantasyflightgames.com/en/products/android-netrunner-the-card-game/), a game set in a dystopian, sci-fi future where MNCs control the world and a group of hackers attempt to hack into those servers for their own personal reasons.

# Project Information
There is a [slack group](https://jinteki.slack.com/) for developers to ask for help or discuss improvements what improvements they want to add. Invitation is gained by submitting a PR. There is also a setup guide as well as some documentation located over at [/wiki page](https://github.com/mtgred/netrunner/wiki/Getting-Started-with-Development).  It has decent [documentation](https://github.com/mtgred/netrunner/wiki/Card-definitions) and [videos](https://github.com/mtgred/netrunner/wiki/Getting-Started-with-Development#videos-currently-behind-a-paywall) on how someone went through bug fixing. The [workflow](https://github.com/mtgred/netrunner/wiki/Contributing-New-Cards) is like most other projects – post in an issue if you want to work on it, then submit a PR when you’re ready. It goes through a review process and gets merged after if it passes.

## Documents
- [Project Readme](https://github.com/mtgred/netrunner/blob/master/README.md)
- [Contributing Guide](https://github.com/mtgred/netrunner/blob/master/CONTRIBUTING.md)

Most of the documentation and information about the project, however, can be found on the wiki page.
- [Getting started](https://github.com/mtgred/netrunner/wiki/Getting-Started-with-Development)
- [Writing Tests](https://github.com/mtgred/netrunner/wiki/Tests)
- [Progress Reports](https://github.com/mtgred/netrunner/wiki/Progress-Reports)
- [User Documentation](https://github.com/mtgred/netrunner/wiki/Jinteki.net-Guide)
- (and more)

# My Contributions
- [Add log entry when Thimblrig is moved #4013](https://github.com/mtgred/netrunner/pull/4013)
- [Fix research grant to work with team sponsorship #4016](https://github.com/mtgred/netrunner/pull/4016)
- [Add tests for research grant #4022](https://github.com/mtgred/netrunner/pull/4022)
- [Add toast prompt for Mti Mwekundu: Life Improved #4024](https://github.com/mtgred/netrunner/pull/4024)
- Issue: [Dadiana Chacon doesn't trash itself if runner drops to 0c after trace #4012](https://github.com/mtgred/netrunner/issues/4012)

# Learning points

## Clojure
My main learning points from contributing to the project is learning **how to use Clojure**, a lisp-like language. Since Lisp and its variants are very different from the programming languages that I have learnt, some tasks in which I thought were easy to do has ended up taking days just to figure out what had to be done. However, through contributing to this project I’ve come to appreciate the use of Clojure in the macro level. While working on the project, it seemed like I was building the game **in a language that was built to build the game**, similar to how game companies build their own custom game engines for their games, this felt as if I was working on a game engine built to create Netrunner – yet that was obviously impossible, since the project was built on Clojure, not a game engine. Yet, due to the way the language used macros and virtual functions for metaprogramming, it felt like I was not working in Clojure, but a game engine built for Netrunner.

## Fixing problems in an unfamiliar codebase
Many of the issues that I attempted to fix was resolved by thinking of a similar card that does a similar function, and then trying to adapt that function over to the actual card. The simplest example is when I tried to implement <tooltip content="[Click]: Place 1 power counter on this upgrade. As an additional cost to run this server, the Runner must spend 1 [Click] and 1 [Credit] for each hosted power counter. When your turn begins, remove all hosted power counters.">[Cold Site Server](https://netrunnerdb.com/en/card/26038)</tooltip>, where I heavily referred to <tooltip content="As an additional cost to make a run on this server, the Runner must spend [Click].">[Ruhr Valley](https://netrunnerdb.com/en/card/02111)</tooltip> for implementation details. Unfortunately, that implementation failed because [Ruhr valley was bugged](https://github.com/mtgred/netrunner/issues/2109), which led to a wrong implementation for Cold Site Server. <br />
It turns out other people used this method too to fix bugs and add features:
![image](https://user-images.githubusercontent.com/4904988/55064985-f28adc00-50b5-11e9-8ff6-a95cbae1446f.png)

## Feeling Involved
Another important thing I learnt while working on the project was the importance of communication between all the members of the development team. The slack channel set up for Netrunner is the main source of communication for all developers, and thus everything goes into the channel, be it thoughts on future development/features, further insight into code snippets or questions on how to do X. Since everything is communicated there, it acts as a **big source of motivation** to work on the project as well, since you read about others implementing feature X and Y or fixing some bug, which really motivates me to do the same. Furthermore, discussions on what is planned helps developers to be involved in the future direction of the project. I feel that this is hugely important to help **encourage new contributors to stay and continue with the project**, otherwise they would feel like they are just being used to implement new features or fix bugs that no one else wants to do and thus was assigned to them.

# Suggestions for internal project

## Involvement
I feel that keeping people involved through discussions on the future of the project, or what is going on within the development team is a very important practice that teammates can adopt. This is particularly true especially since teammates (and other NUS-OSS project) gets a yearly infusion of people to work on the project, which no other open source project has. Due to this, teammates have grown differently from other projects. Since most contributors live in Singapore, **many discussions on teammates happen offline**, be it requests for help or new features. Sometimes, they occur in private slack channels. Despite Teammates's OSS policy (wherein it is said they they'd prefer to discuss everything openly, using the issue tracker as a forum) there are many things that don't go on there. Since they don't happen online, others can't find them if they're encountering the same issue. Additionally, because other developers don’t get to listen in on what the senior developers are discussing, it is harder for them to see the bigger picture. Losing this main channel in which all developers are included loses a lot of the motivation that people get when working on the project. It is hard not to **feel as an employee of the project** when all that is done is that you are assigned tasks to complete, in which after completion you are assigned a new task. You only get to see glimpses into a small part of the project. This difference in how teammates is organized, unlike other OSS, is what I think Teammates’s biggest problem is, and why it has such trouble in retaining people to work on the project.

## Documentation consolidation
Unlike teammates, Netrunner has all its documentation in a single location, located under the wiki page. This provides several advantages:
* Documentation is all consolidated in one place, making it easier to find what you want - when I was looking for documentation in the project, I simply had to go to the wiki page and check the table of contents for what I need. However, with teammates, documentation is scattered all over the readme file, **some embedded within several layers of links**. I think that teammates would derive a large benefit from having all its documentation easily found and consolidated in one place rather than having developers search for it (sometimes with Google!)

* Ease of editing. Through the wiki pages, Netrunner's documentation can be easily editable, without the need to go through a PR and make changes. For example, when I found an event hook that was not listed in the wiki, I was able to simply click `Edit` on the wiki page and add the event hook myself. This made it easy and seamless to update the documentation of the project.

