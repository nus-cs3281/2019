### Project: 
* [Kentico Cloud Swift SDK](https://github.com/Kentico/cloud-sdk-swift/blob/master/CONTRIBUTING.md) 

### Documentation: 
* [Ways to contribute](https://github.com/Kentico/cloud-sdk-swift/blob/master/CONTRIBUTING.md)
* [Submit pull requests](https://github.com/Kentico/cloud-sdk-swift/blob/master/CONTRIBUTING.md#submitting-pull-requests) 


### Contribution so far:
* [Fix Xcode warnings](https://github.com/Kentico/cloud-sdk-swift/pull/64)
* [Implement retry policy](https://github.com/Kentico/cloud-sdk-swift/pull/63)
* [Implement image URL builder](https://github.com/Kentico/cloud-sdk-swift/pull/68)

### Observation:

 * As shown in the above documentation link, they also use the [feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow), which is similar as TEAMMATE's. 

* The KenticoCloud iOS SDK developed by [Kentico CMS](https://www.kentico.com/) is a Swift library used for retrieving web content. Since the SDK is target to developers rather than general users, the documentation is quite detailed in terms of both developer guide and inline comment. As shown in this [link](https://github.com/Kentico/cloud-sdk-swift/blob/master/CONTRIBUTING.md#Definition-of-Done), they require documentation in every `public` member in order to make it clear for other developers.

### What I have learnt

* **Write meaningful commit message and organize commit messages well.** I found it important because as I used to have messy commit messages, sometimes I even confused myself when I wanted to track some files. Organizing commit message is quite a valuable skill that I learnt from contributing to open source project. TEAMMATE also emphesis organzing commit messages.

* **Read documentation of dependencies, and be careful to block main thread.** In this [PR](https://github.com/Kentico/cloud-sdk-swift/pull/63), my first approach blocked the main thread, which was pointed by the maintainer. He also told me to read some documentation of dependency modules, and finally I implemented better functionality. Sometimes the dependencies have provided API that can solve the issue. I should explore them before implementating the feature from scratch.

* **Follow some [contribution etiquette](https://tirania.org/blog/archive/2010/Dec-31.html).** This is written in thier contribution guide. I used to try to refactor the code for my better understanding before fixing the issue. However, I realize that applying this will cost extra effort for maintainer to review my refactoring, and is not a good practice to contribute to open source project. This link about etiquette can also be put on TEAMMATE since it will be contribute to large number of developers.

### Tools
* Auto-generating documentation: [jazzy](https://github.com/realm/jazzy)
* Testing: [Quick/Nimble](https://github.com/Quick/Nimble)

However, after exploration, these framework are typically designed for Swift/Objecive-C. Therefore, it is not applicable to NUS-OSS project currently. However, there are similar tools that support for other languages, such as `Javadoc` which can be used for TEAMMATE.

### Suggestions to TEAMMATE
TEAMMATE can pay more attention to documentation, especially the developer guide. As an API developer, I often find it costing a lot of time to understand how does the API work, and try to consolidate it.
Since TEAMMATE is intended to be contributed by a large number of developers, it is important to help them understand the codebase quickly. Therefore, I believe the developer guide on API layer is necessary for both backend developers to improve the API and frontend developers to use API. It will be better if the developer guide on storage lay can also be provided.  




