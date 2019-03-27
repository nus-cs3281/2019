**Project**: [Exercism](https://github.com/exercism)

# My Contributions
- [Add a completely new exercise, the Knapsack Problem](https://github.com/exercism/problem-specifications/pull/1484)
- [Convert an existing exercise, Pascal's Triangle to C++](https://github.com/exercism/cpp/pull/235)

# What is Exercism?

Exercism (https://exercism.io) is an online open-source coding platform that offers coding practice and mentorship for over 40 programming languages! As of August 2018, Exercism has 1,700 contributors and 700 mentors.

### Contributing to Exercism
- [Finding your way](https://github.com/exercism/docs/blob/master/finding-your-way.md)
- [Contributing to language tracks](https://github.com/exercism/docs/blob/master/contributing-to-language-tracks/README.md)

# Key Takeaways

Exercism is a good choice for new contributors. Exercism has a nice variety of issues for newcomers to contribute to and excellent documentation to match as well. A few ones someone can start contributing to this repository include:
- Improve existing tests for an exercise
- Convert an existing exercise to another language
- Create your own exercise
- Improve grammer/phrasing for exisiting exercise
- Help maintain or fix bug in build systems/tools

As you can see, there is a range of issues one can work one. The issues can range in difficulty from trivial to really challenging. I chose to do one simple Pull Request(PR) to port an existing exercise to C++ and I did a slightly harder PR which involved creating a brand new exercise. There have been many learning points throughout this process. I will list some of the more important ones and eventually compare them with my internal project, Teammates.

### 1. The more the merrier...or is it?

Exercism has over 40 programming languages and has a repository specifically for an exercise. There is one master repository that handles the canonical data for all the exercises. There is a certain elegance to how this project has managed to keep a decentralized system like this working. There are core team members working on each repository and each track has specific instructions on how to set-up and create new exercises. 

My contribution to C++ for example uses `CMake` to test the code and has a specific format for the files. I knew this from the clear documentation they provided. The team responded almost immediately to my pull request and merged it in after a couple of seconds. It was all very smooth. 

How does one manage such a decentralized system effectively? Exercism also definitely has its ups and downs.. but for the most part it does a fantastic job of syncing across the different programming languages for the various exercises. It is able to do so because of a strong team (some of them I believe are volunteers) who are willing to spend their spare time guiding new contributors and maintain the repository. More than just the technical aspects, I have learnt that it is the people who drive large open-source projects; people with a core mission and passion to work for a larger cause.

### 2. Pushing the difficulty barrier.... Code Quality/Checks 

While I was doing the PR to port an existing exercise to C++, I realised I was just following a routine. Yes, I learnt about the contribution workflow and the development process behind Exercism. However, I could not help but wonder if this project had good quality control or stringent reviews. Majority of their PRs are small patches and I did not see much of this. As a result, I tried something different and implemented a completely new exercise. 

This is a big deal. Mainly because a new exercise will be something that is going to be shared over all the 40+ languages. Every other language will be using your data and description. I submitted a PR to add a classic problem: the 0-1 knapsack. 

Over the next few days, I was hit with a series of consecutive reviews. I had six people in total commenting on my PR. The reviewers were thorough. Some wanted to be convinced on why this exercise was needed. Others tore my description/tests down and asked those parts to be updated. 

Overall, I have to say this project enforces a high standard for their exercises. What really impressed me was how 6 people reviewed by PR without having too much conflict or overlap. Each of the reviewers took the time to sit and read through the exericse/problem and point out subtle details. One of the reviewers updated some parts himself and pushed into my branch! (He told me the changes he made and his rationale) What i have learnt from this is as a reviewer, it is important to justify your comments and also convince the person contributing on why a change is needed. If you look at my PR on this above, you would realise that all the reviewers justified their comments and even asked for my opionion on changes. This is how you encourage new contributors to contribute further and grow your developer teams. I look forward to contributing more to them.

### 3. The bigger picture - Teamates vs Exercism

Now that I have covered some of my major takeaways, it is important to take a closer look at how my journey with Exercism compares with my internal project Teammates.

#### a. Encouraging development from the outside

Teamamates does not do a good job with encouraging new contributors as compared to Exercism. Of course, this is not a fair comparison considering teammates is still undergoing migration and there are specific deadlines to meet. 

However, in the long run, I feel Teammates should strive to be inclusive to any external developer. This means improving our documentation and opening doors to a large variety of issues for one to work on. Similar to Exercism, Teammates should have a path set to allow new contributors to rise up the ranks and perhaps even become one of the core team members. 

A more convenient set-up and testing framework would be ideal as well. Exercism has make files and tools to allow developers to quikly start contributing. 

#### b. Strive for innovation and try to look past the conventional path

This is a strong point. However, what I really want to say is that Teammates sometimes suffers from a lack of innovation. We follow what we are told to do and follow tasks simply based on protocol. There is not much room for innovation and in fact, there is very little encouragement to come up with newer ideas.

Exercism leaves room for someone complemetely new to come in and start something. I came in with a brand new exercise and I was encouraged by the team. Teammates should also look to encourage innovation. It is only by having people who can look past the ordinary path, can growth be achieved. Many times I feel that new ideas are shot down too quickly or are looked past citing reasons like this is how it was done in the past etc. I hope this will change one day in the future!

**Note**: Exercism is also not perfect and it has its flaws. It is an established project and thus, there is not much change going on. Teammates is in migration and is undergoing massive change. Any comparison is not completely fair.
