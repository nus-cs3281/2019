**Project**: FOSSASIA's chat.susi.ai 

**My Contributions**: 
Pull Requests:
- [#2052] (https://github.com/fossasia/chat.susi.ai/pull/2052) 
- [#2068] (https://github.com/fossasia/chat.susi.ai/pull/2068)

Issues:
- [#2067] (https://github.com/fossasia/chat.susi.ai/issues/2067)
- [#2051] (https://github.com/fossasia/chat.susi.ai/issues/2051)

**Documentation**:
 Contributor Guide: included as part of the [README](https://github.com/fossasia/chat.susi.ai/blob/master/README.md)

**Observations**:
FOSSASIA's SUSI.AI is an artificial intelligence system, combining pattern matching, internet data, data flow, and inference engine principles. Since chat.susi.ai has consistently been a Google Summer of Code project, and FOSSASIA has a reputation for being open towards first-time contributors, I thought it'll be a good experience. I also wanted to diversify and try new things - since I had had experience with VueJS, and was doing Angular in my internal project, I thought the ReactJS based chat.susi.ai would be the best option for me. 

#### Frameworks:

The chat.susi.ai is a front-end developed for web access of SUSI, and is written in ReactJS. Right out of the gate, I noted the difference in the choice of front-end frameworks between my external and internal project. Since I primarily worked on the front-end for both projects, I noted that ReactJS is significantly easier and has a much gentler curve as compared to Angular. Since TEAMMATES aims to be a student-driven project, I have fairly mixed feelings about our decision to use Angular.

#### Contributing:

While their contributor guide is very barebones compared to TEAMMATES's extensive guide, their project is actually fairly easy to set-up, and has significantly fewer rules. Their coding style is actually fairly inconsistent, unlike TEAMMATES, which has a very stringent lint. I wouldn't categorise either as good or bad, since both work just fine.

chat.susi.ai also is also less welcoming to first-timers, with no issues being flagged as first timer issues. Instead, they have a very unusual system where most contributors point out missing features themselves, and state in the issue description that they are working on the missing features (in fact, the default message for opening an issue already includes the question 'Do you want to work on it?'). I definitely prefer TEAMMATES's approach, where relevant issues that are currently the focus of the team are flagged out for first timers. They also take significantly longer to respond to PRs and queries on average.  

They also have multiple reviewers per Pull Request, and it is very disorienting to try to please all competing reviews on your Pull Requests. This is stark contrast to TEAMMATES, where the Project Lead strictly told us that no more than 2 contributors should review any PR, unless there is a very glaring error that has to be pointed out. This ensures that the person making the PR is not trying to juggle multiple competing suggestions at once. 
 
However, as a project with a more established front-end, they do have some very nice features that would be great for TEAMMATES.

Particularly mention-worthy would be surge.sh, which is a website that allows you to quickly deploy your front-end on a URL for free. All PRs made to chat.susi.ai require you to mention the surge.sh link the project is deployed to, and the reviewers will look through the actual front-end. This, in my opinion, is better than the snapshot tests we are currently running on auto-update mode to test the rendered final product, as it is significantly easier to just look at the web page, instead of trawling through thousands of lines of HTML. I think TEAMMATES will greatly benefit by combining the use of surge.sh (or similar platforms like netlify) and snapshot tests, as we can hasten the process of looking through the rendered snapshot for the 'ideal' case, and all subsequent checks can be done against an 'ideal' snapshot quickly (snapshot tests will still be needed to test all 'other' cases, but since they are less likely than the ideal scenario, it should still reduce the review workload significantly). I understand that the logistics of this will be fairly challenging, but we can explore options such as making stubs for all the API endpoints, among other things, especially given that our front-end is in such a nascent stage. 

#### Takeaways

While I certainly learned a lot about ReactJS and CSS for the purposes of making this contribution, I learned much more about how to be better reviewer, as I understood the shortcomings of a relatively poorer reviewing system. I learned that it is crucial to be enthusiastic and supportive towards contributors, as it encourages them to continue not only towards this specific project, but also Open-Source projects in general, and that we should definitely ensure that our committers have a bit more guidance when they first come onboard and start managing the project, as the reviewing process can really shape the experience of contributors. 

