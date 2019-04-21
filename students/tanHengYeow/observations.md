## External Project: [Firefox Developer Tools](https://firefox-dev.tools/)

### Contributions
1. Summary of [bugs](https://bugzilla.mozilla.org/buglist.cgi?query_format=advanced&emailtype1=exact&emailassigned_to1=1&email1=E0032242%40u.nus.edu&list_id=14599249) worked on
2. Summary of [other contributions](https://bugzilla.mozilla.org/buglist.cgi?query_format=advanced&emailtype1=exact&emaillongdesc1=1&email1=E0032242%40u.nus.edu&list_id=14636163) made e.g. bug triage, raising bugs, performing code reviews, technical assistance, helping contributors etc
3. [Profile page](https://bugzilla.mozilla.org/user_profile?user_id=624287) gauging level of activity

### Contributing workflow

There is a comprehensive [developer documentation](https://docs.firefox-dev.tools/) that one can consult for working on Firefox Developer Tools (FDT). I will give a summary of only the necessary steps required for the typical contributing workflow.

1. [Set up a Bugzilla account](https://docs.firefox-dev.tools/getting-started/bugzilla.html). Bugzilla is Mozilla's bug tracker.
2. Use [Mercurial](https://www.mercurial-scm.org/) as the Version Control System (VCS), [pull and build](https://docs.firefox-dev.tools/getting-started/build.html) the code.
3. Find suitable bugs to work from this [page](https://bugs.firefox-dev.tools/?easy&tool=all). You can also use [Codetribute](https://codetribute.mozilla.org/projects/devtools) to find good first bugs to work on.
4. Run [browser mochitests](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Mochitest) to check for regressions after making code changes.
5. Use [Arcanist](https://moz-conduit.readthedocs.io/en/latest/arcanist-user.html) or [moz-phab](https://moz-conduit.readthedocs.io/en/latest/phabricator-user.html#using-moz-phab) as a command line tool to manage code reviews performed in [Phabricator](https://moz-conduit.readthedocs.io/en/latest/phabricator-user.html#creating-an-account), a suite of web-based software development collaboration tools.

### Learning points

Throughout my journey in contributing to FDT, there are many learning points that helped me become a better open source contributor, which are also beneficial for other engineers alike.

1. Produce clear Steps to Reproduce (STR)

The STR can refer to steps on reproducing a bug or steps of how one goes about debugging or testing code manually. This is especially important for projects like FDT where it involves a variety of different expertise. They include people working on different panels of FDT, people working on front-end and/or back-end of FDT, people working on the networking platform, people working on localization/accessibility, people working on other parts of Firefox and external contributors with different backgrounds etc.

Different expertise possesses differing context of the issue at hand. As a result, without a clear STR, it would be hard to involve different expertise to collaborate together to solve an issue.

Take for an example this [patch](https://bugzilla.mozilla.org/show_bug.cgi?id=1493599) which involves the back-end platform team exposing an API to the front-end team to use. As both the front-end and back-end codebase's size are significantly huge, different people in different teams may have little idea on how things work specifically in each other's domain.

A good example would be this [comment](https://bugzilla.mozilla.org/show_bug.cgi?id=1493599#c9) where it clearly describes the STR of how the code is tested so that expertise from the other team has a better idea of the context of one's approach in performing the manual test.

As a general rule of thumb, I learned that we should be as verbose as possible in giving STR, to the extent where we put ourselves in the receiving party's shoes and assume they do not have any prior knowledge.

2. DevOps expertise is crucial

FDT is a complex web application embedded within Firefox, both of which have significantly large codebases. A dedicated system [Treeherder](https://wiki.mozilla.org/EngineeringProductivity/Projects/Treeherder) is built to handle Continuous Integration (CI) data, which similar to the Travis CI that we use in NUS-OSS.

Reviewers would normally push ongoing patches to Treeherder (with an estimated of ~1 hour of build time) to check for regressions before reviewing the patch. Contributors who fixed a few bugs are allowed [Level 1 Access](https://www.mozilla.org/en-US/about/governance/policies/commit/access-policy/), which enables them to push their patch to Treeherder to check for regressions.

With proper CI in place, reviewers can ensure that the submitted patch does not cause the software's build process to fail. This is crucial where the consequence of regressions is very heavy as a small breaking change might cause the Firefox browser to malfunction.

With millions of people pushing new code/features to the same codebase every day, the importance of DevOps team is obvious here because they are responsible for landing the code in the codebase while ensuring that the codebase stays healthy.

Even though one can rely on automated CI software that is managed by external vendors, having DevOps knowledge would ensure that a team can build, test, and release software faster and more reliable as the product scales.

This is a [case study](https://amido.com/blog/a-case-study-of-devops-at-netflix/) from Netflix on how DevOps is practiced in the company.

3. Using Test-Driven Development (TDD)

Almost every bug that I worked on for FDT required me to write a test to verify its functionality. Occasionally, I'm required to make changes to other test files as well due to the code changes I made.

The reason for writing tests is because regression testing is needed to ensure that we do not break other features present in the codebase during the build process (related to the previous point above on DevOps).

Tests are heavily encouraged in software that utilizes DevOps, thus it would be more efficient for developers to use TDD.

Instead of thinking of writing tests as an afterthought, reversing the process would result in increased productivity.

4. Having an active international community of members result in higher contributor retention rate

FDT has a dedicated Slack [channel](https://devtools-html-slack.herokuapp.com/) which has different channels catered for different panels and a general channel catered for everyone.

At any point in time, there is a high chance that one's query is answered by a member that is online. Over time, this behavior encourages people to give back because they have received some sort of help from others in the same way too.

Also, by having an active community of members giving back their knowledge, it encourages new contributors to be less reluctant to ask questions for fear that they might be asking "stupid" questions or just embarrassed that they will be judged based on what they ask.

Furthermore, actual Mozilla employees communicate with other contributors in the same channel as well and often aid new contributors with basic queries. This act also reflects well on the community on welcoming new contributors.

### Transferable knowledge

Throughout my journey in contributing to FDT, there are a few points that I feel TEAMMATES can adopt as well.

1. Have a list of experts in certain areas of the codebase

In FDT, there are owners for different panels. They are the main person(s) to go to or get reviews from when working on a respective panel.

Even though the scale of TEAMMATES may be smaller, there is still an incentive to have this type of structure. In the past, issues are grouped based on different areas of the TEAMMATES for e.g. `f-Results`, `f-Questions`, `f-Profiles` etc. Also, we have past area leads who led certain areas of TEAMMATES.

However, the recent ongoing migration to v7 requires most contributors to work with multiple areas of TEAMMATES and issues are mostly grouped according to front-end and back-end.

We can definitely consider bringing back this structure once the v7 migration has been completed. As the project gets bigger, it is hard for one to know everything, with the exception of project leads which require years of experience.

New contributors can start off understanding certain areas of TEAMMATES and then slowly branch out to more areas of TEAMMATES. They can then choose 1 or a few areas to be an expert at after working with the codebase for some time. Afterward, they would help in handling reviews, suggestions and/or provide directions for features related to their area of expertise.

2. Maintain a technical blog

FDT maintains a [technical blog](https://hacks.mozilla.org/category/developer-tools/) which highlights their roadmap, new features and also retrospections.

We can set up a technical blog for TEAMMATES highlighting our milestones and achievements based on the releases we made. There are a few benefits to doing this.

Firstly, it provides students a chance to improve their technical writing skills and also share the work that they have done with more people.

Also, having a technical blog provides a platform for potential contributors to be aware of TEAMMATES, the tech stack we are using and also the impact that we are making for educators worldwide. This allows TEAMMATES to get noticed by new contributors and might result in a potential source of constant contributors apart from Google Summer of Code (GSoC), CS3282 and summer interns.

Lastly, having a technical blog would also reach out to a wider range of audience. Software rarely gets noticed through GitHub repositories. Having a platform that reaches out to a wider range of audience could bring in more users, potential sponsors and also opportunities for collaboration.

3. Online video call meetings

In FDT, they hold team weekly video calls with meeting notes recorded. This might be hard to reproduce exactly for TEAMMATES due to the difficulty in accommodating to everyone's schedule.

However, one recommended approach I can suggest would be to hold a video call meetings for significant milestones that involves external contributors too. Right now the only meeting that TEAMMATES does is the code sprint to get everyone up to speed to develop for TEAMMATES during CS3282. Even so, they are catered for our own NUS students.

External overseas contributors rarely get a chance to deal with significant milestones that the TEAMMATES core team is handling with the exception of GSoC students where they take on a significant project over the summer.

The retention rate of past GSoC students is low, as well as external contributors who often fix a few bugs for coursework and leave afterward.

By having video call meetings for significant milestones that TEAMMATES is working on, we can also involve external contributors so that most of the people that are committed will be on the same page and would not feel left out.

I feel that retaining external contributors would be a good first step in getting more mentors to handle more potential CS3282 students. Over time, I believe retaining external contributors would form a virtuous cycle of increasing the number of contributors for TEAMMATES.

4. Issues that are harder than first-timer issues that involve more mentoring

From my observations, our `d.firstTimers` issues are a lot simpler than other projects but the transition to work on `d.Contributors` issues may be huge for some contributors.

For contributors that require more assistance and time in understanding the codebase, they would often give up after solving their first issue and then stop contributing. However, they might turn out to be effective contributors given more time to understand the codebase.

We can take inspiration from FDT's [profiler](https://github.com/firefox-devtools/profiler) where both their `good-first-issue` and `help wanted` [labeled](https://github.com/firefox-devtools/profiler/labels) issues involve instructions on how to complete the task.

Although finding the related files to change is part of the learning process, we can identify some of these bugs and provide clear instructions on how to proceed to work on it. This would give potential contributors more confidence to take on harder issues. As a result, the transition from a `d.firstTimers` issue to a `d.Contributors` issue would be smoother.

5. Active Slack channel that welcomes external contributors too

Right now our Slack channel only accepts interns and CS3282 students due to mentoring resources available.

The initial phase of mentoring these external contributors may require a lot of resources and there is no certainty that they would stay too. However, if we think of this issue in another perspective, having external contributors invited to the Slack channel might benefit TEAMMATES in the long run.

Firstly, it allows current CS3282 students to have a chance to mentor external contributors. New contributors to the project helping each other sparks positive interactions and would contribute to an increased retention rate of contributors. Over time, the interaction might scale up to the level of what FDT has currently, which is a win-win situation for everyone.

Also, there are little drawbacks to accepting external contributors even if they do not become active contributors in the end. That would be almost equivalent to having little to no external contributors in the first place.

We can have a separate TEAMMATES public channel to start the ball rolling if there are concerns integrating this suggestion into the current channel we have now.

### Areas of improvement for external project

1. Provide more architectural diagrams

Most of the documentation is text-based which might be hard for new contributors to follow. Architectural diagrams or diagrams, in general, would help contributors in understanding the codebase in a visual manner, similar to what TEAMMATES have currently done.

In addition, diagrams also provide more experienced contributors an easier reference to work with. Furthermore, it can be used to facilitate technical onboarding of new members/employees.

2. Incrementally move to a more well-known VCS like GitHub

The act of moving code to GitHub attracts more contributors as the code would have more visibility given that more projects are now on GitHub.

Also, most people are familiar with Git rather than Mercurial, so that adds up to attracting contributors.

There is an ongoing initiative to do that as seen by the debugger living in a GitHub [repo](https://github.com/firefox-devtools), so that is definitely a step in the right direction.
