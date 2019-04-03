**Project**: [PHPMyAdmin](https://github.com/phpmyadmin/phpmyadmin)

**My contributions**:
- [ExportJson: prevent crash when encode returns boolean #14930](https://github.com/phpmyadmin/phpmyadmin/pull/14930)
- [Add check for empty input to change_collation #15031](https://github.com/phpmyadmin/phpmyadmin/pull/15031)
- [Improve grammar in Validator #15049](https://github.com/phpmyadmin/phpmyadmin/pull/15049)

**Introduction**

PHPMyAdmin is an open-sourced web interface for MySQL and MariaDB. As a portable web application written primarily in PHP, it has become one of the most popular MySQL administration tools, especially for web hosting services.
I chose to contribute to PHPMyAdmin because it is one of the first tools I have ever used when I first learnt Web Development, and it would be meaningful for me to contribute back to the tool that has served me well for many years. Furthermore, given its large user base and nature of operations, it is important for PHPMyAdmin to engineer a reliable and secure product. This is where I had hoped to learn best reliability and security practices and apply them to my own projects.
I am also very comfortable with the language, having used PHP primarily prior to picking up more recent languages like NodeJS.

**Key takeaways**

The PHPMyAdmin community has a similar process to many of the projects I've worked on, yet there are many small details that pondered reflection.

**#1** In very large projects, it is important to write code in a clean manner.
PHPMyAdmin uses automatic tools to check for code quality and style. In addition, there is strong emphasis on writing code in classes. The nature of the underlying language, PHP, is not very OOP-focused. However, PHPMyAdmin uses many classes (e.g. forms, databases, tables etc) to abstract and simplify implementation. There is also strong evidence of reuse: constant strings, form generators, database abstractions that break down the code into much more manageable chunks.
Even as a new developer, I had little trouble diving into PHPMyAdmin to fix bugs and add checks because it is easy to trace and understand the role of each function and each class.

In contrast to my projects,
SE-EDU: AB4's code is extremely clean and each function has its own dedicated role. With a core focus on developing as a model for teaching Software Engineering, AB4 focuses on writing our code to strictly follow OOP guidelines. However, I wonder if there is over-engineering in AB4. In PHPMyAdmin, there is a strong sense of structure - each class does its own unique role. However, things like single responsibility principle are not as strictly enforced. While these principles seem to make code cleaner, we must also remember that if the role of each function is so small, it takes more effort for a developer to trace through the code and to have a global picture of the flow in the program.

MarkBind: MarkBind's code is certainly less clean than PHPMyAdmin. Even after 10 weeks of developin in MarkBind, I still have to repeatedly trace through code to understand the process. Sometimes, I need to even consult senior developers to understand how MarkBind simply "magically" works. This is a sign that MarkBind would need more emphasis on code maintainability. Perhaps we need to rewrite some of our functions and features as smaller, more cohesive classes. 

**#2** Commit messages should be descriptive, but not overly complex.

As with most Software Engineering project, high quality commit messages are a key part of Open Source Software. Commit messages allow future developers to understand why certain design decisions were made, providing a snapshot in history to make changes based on.
PHPMyAdmin is no different - every commit needs a corresponding descriptive commit message explaining the change. 

However, this commit message "rule" is also not strictly enforced. While I try to provide convincing reasons behind the need for each commit, some developers see less point in writing a descriptive commit message. It appears that these commits are merged anyway.

My experience at SE-EDU has trained me to write highly descriptive commit messages that served to convince maintainers the reason behind every commit. This is in stark contrast to commits at PHPMyAdmin or MarkBind, where developers simply need to provide a descpriton of their commit. For PHPMyAdmin, developers can even sometimes get away without writing significant commit messages.
This has prompted me to reflect on why SE-EDU has adopted such a requirement for commit messages. 
On one hand, as a role model for Software Engineering, the project serves to teach new developers the "right" way. Leading by example, these messages explain commits so well that the project can be easily understood by anyone.
On the other hand, such a system slows down development. Given that every commit needs to be tightly scoped and must accompany such an extensive commit message, the impedence to change is very high and developement cycles are slow.
Perhaps, for an average Software Engineering project, a system similar to that of MarkBind would be ideal. While there is no fixed format and fixed requirement, developers are required to write messages that are informative and descriptive. Such an option finds a middle ground that balances ease of development and quality.

**#3** It may not be feasible to enforce good SE practices when a project grows large.

The key driving component behind every Open Source Software is the quality of its commits. Like every other OSS, PhpMyAdmin uses CI tools to automate the process of code checking.
This process is similar to my other projects: MarkBind and SE-EDU where we use CI extensively to do testing.

I notice that while tests play an important role in PhpMyAdmin (some are necessary to assure functionality, others important for security), the test coverage is surprisingly low at [52%](https://codecov.io/gh/phpmyadmin/phpmyadmin).
This could perhaps be due to the fact that PhpMyAdmin has so many contributors (almost 1000) and PRs on a daily basis. Having strict requirements for testing meant that it would be heavily resource intensive to ensure that new PRs are done properly with tests. In addition, this might also mean sacrificing development speed. This might further delay the release cycle and ability for the organisation to respond quickly to fixes and other updates. Being a long-time legacy project of 20 years, PhpMyAdmin started during an era where idea of testing has not yet been popular, contributing to its current poor coverage.

I wonder if it's necessary to sacrifice "proper" software engineering practices if we want our project to expand in scale or to hasten the development process.
For example, the high quality required by SE-EDU means that commits go through extensive revisions, small changes need to be accompanied by high overhead like commit messages, tests and documentation. The high impedence to change means that some developers could potentially avoid contributing because of the hassle.
At the end of the day, it is the project that determines the its own priority. Then projects that focus and require reliability and quality would certainly place greater emphasis on them, mandating tests and proper coding practices. It appears in this case that this is perhaps not the focus for PHPMyAdmin.

Reflecting upon MarkBind and SE-EDU, I find that both CS3282 projects are heavily tested. For MarkBind, our scale is still relatively small with significant amount of resources available to ensure reliability. On the other hand, SE-EDU/AB4 is a role model for Software Engineering. It makes sense that these projects have reliable and extensive tests, and I see little reason to change.