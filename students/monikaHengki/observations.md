**Project**: [Mozilla Firefox](https://hg.mozilla.org/mozilla-central)

**My contributions**:
- [Enable ESLint for dom/cache (automatic changes)](https://phabricator.services.mozilla.com/D20943)
- [Enable ESLint for dom/cache (manual changes)](https://phabricator.services.mozilla.com/D20944)
- [Drop support for PageThumbUtils.createCanvas with null window](https://phabricator.services.mozilla.com/D22892)

**Documentation**:
- [Developer Guide](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide)
- [How to submit a patch](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/How_to_Submit_a_Patch)

**Tools**:
- VCS: [Mercurial](https://developer.mozilla.org/en-US/docs/Mozilla/Mercurial)
- Bugtracker: [Bugzilla](https://bugzilla.mozilla.org/home)
- CLI tool to submit patches: [moz-phab](https://github.com/mozilla-conduit/review)
- Patch review: [Phabricator](https://phabricator.services.mozilla.com/)

**Observations**

Mozilla Firefox is is a free and open-source web browser developed by The Mozilla Foundation and its subsidiary, Mozilla Corporation. I chose to contribute to Firefox because I wanted to be involved in one of the largest open source projects. Because of this scale, I can find [many ways where I can contribute](https://codetribute.mozilla.org/) based on the language I am comfortable in (Javascript and Java).

**Key takeaways**

Throughout the process, I have learnt a few lessons not only as a contributor, but also as a maintainer of an open source project.

**#1** It is important to have **an active community of developers who are ready to help**.

As a new contributor to Mozilla, the biggest obstacle I faced was getting used to the tools used in the workflow. I am used to `git` for version control (VCS), and `Github` as the bugtracker, PR tracker, and repository storage. However, Mozilla uses `mercurial` for VCS, `Bugzilla` to track bugs, `moz-phab` to submit patches, and `Phabricator` to review patches. Not only did setting up the project take some time, but the difference in tools used also created extra hurdles to me. Although the tools are quite well documented, the amount of documentations I had to read were overwhelming especially to new contributors.

Even when I faced these challenges, help was readily available. There is an [IRC channel](https://wiki.mozilla.org/IRC) dedicated to help new contributors get started. I have asked some mercurial-related questions and within 5 minutes, my questions were answered by an experienced developer from the community. Furthermore, many of the bugs were mentored. I was fortunate enough to work with a mentor who helped me as I was fixing my first bug. Even after my first patch got accepted, he willingly suggested other bugs that I can work on. The community felt very welcoming, and this definitely helped to attract and retain new contributors.

**#2** Always write **clear documentation for your code**

I observed that the documentation in the codebase is very extensive. For instance, in [this part of the code](https://searchfox.org/mozilla-central/source/toolkit/components/thumbnails/PageThumbs.jsm#610-619), the documentation not only mentions why certain things are being done, it also mentions related bug numbers that the person should refer to. This is helpful especially because the codebase in Mozilla is extremely huge, and it is impossible for someone to always keep track of all the code changes.

**Suggestions for TEAMMATES**:

From contributing to Mozilla, here are some ways practices that TEAMMATES can adopt.

**#1** Have a **communication channel for the public**

As for now, the main communication channel used is Slack, and it is only for contributors from CS3282. It could perhaps be useful to allocate a separate Slack channel that is open to public so that new contributors can communicate directly to the maintainers. Not only would this make newcomers feel more welcome, it can also better retain new contributors so that they will keep contributing to TEAMMATES.

**#2** Having **mentored bugs** that new contributors can work on

Currently, TEAMMATES encourage new contributors to work on `d.FirstTimers` issue so that they can familiarize themselves with the codebase and the workflow, then move on to more complicated bugs. However, some of the first timer issues such as updating the user-map may not suit new contributors who are already quite experienced and are looking for more challenging bugs. To cater to these people, perhaps TEAMMATES can have a new label for mentored bugs: bugs that are challenging but also comes with a mentor so that more experienced new contributors can work on them.

**Suggestion for Mozilla**:

Perhaps Mozilla can slowly switch from using `mercurial` to using `git` as a VCS, because the number of developers and projects using `mercurial` is much smaller than those who use `git`. This will definitely be easier for new contributors to start getting involved in Mozilla.
