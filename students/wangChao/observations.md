## **Project**: [CheckStyle](https://github.com/checkstyle/checkstyle) 
Checkstyle is a tool for checking Java source code for adherence to a Code Standard or set of validation rules.

### Links
The link of the workflow of contributing to CheckStyle is [here](https://checkstyle.org/contributing.html#Content)

### Contributions made
* [Issue #6381: Incorrect warning for empty lambda bodies with google_checks.xml](https://github.com/checkstyle/checkstyle/pull/6406)
* [Issue #6083: Add Limitation in index.xml.vm](https://github.com/checkstyle/checkstyle/pull/6423)
* [doc: add File Filter section in extending.xml](https://github.com/checkstyle/checkstyle/pull/6433)
* [Issue #6345: RightCurly with option alone false negative for class, method and constructor](https://github.com/checkstyle/checkstyle/pull/6505)
* [Issue #6367: Improve pitest coverage for RightCurly](https://github.com/checkstyle/checkstyle/pull/6614)

### Workflow
The basic workflow is like this: 
1. Submit an issue and wait to be approved or choose an approved issue from the issue list.
2. Work on the issue and squash the changes to one commit.
3. Raise a PR and wait to be reviewed.
4. Edit your PR until being approved by all maintainers.

The workflow of CheckStyle do not have a big difference with RepoSense and SE-EDU.

### Impressive aspects
There are two impressive aspects when I contributes to CheckStyle. One is CI Test, another is Diff Report.

For the CI Test, CheckStyle has 17 checks to pass in order to proceeded with PR. The tests covers a variety of aspects.
For example, it ensures that the project is able to run on all JDK version and all Platforms. Also, it requires the 
code to have 100% coverage. 100% is even not enough for the tests. CheckStyle also have a test named `pitest`, which is
a kind of mutation test. It is basically modifying the test code to look for tests failure. It will find out the lines 
that are able to be modified without tests failure, which indicates either the test case can be improved or the main code
can be improved.

For Diff Report, basically, it ask all the changes related to main code that may cause a regression to generate a diff 
report, which compares the result of analysis generated for a large number of public repos before the change and after 
the change. This process is to ensure that no regression happens after the change. This tool is written by the developer
of checkstyle and it plays an import role in the workflow of CheckStyle.

### Suggestions to RepoSense 
For now, RepoSense do not have a coverage test yet, which may because the test coverage is not satisfying at the early 
stage of RepoSense. Now, we already have a high code coverage, so the previous concern is not true anymore. Also, having 
a coverage test allows us to improve our testing with higher revenue and lower costs. So, maybe RepoSense should integrate 
coverage test now.

We already have a Netlify preview for some Repos which plays a similar row with diff report. However, it is not same.
For now, we basically analyze the preview manually to see if regression happens.
Maybe we can develop a tool that are able to analyze the difference of the two report generated so we can have a better 
insight of potential regressions.

### Suggestions to SE-EDU
Currently, AB4 has coverage test. However, it do not have mutation test. As a project that teaches students about SE 
related knowledge, maybe we can integrate mutation test in our code because it is reasonable to let the students know
that there is another kind of test to test code quality.

Because AB4 is not analysis based application, so a Diff Report is not suitable for AB4. 

### Suggestions to CheckStyle
Firstly, the developer guide of CheckStyle does not give an overall structure of CheckStyle and how each component interacts with others. 
Since CheckStyle has a huge code base, it is quite hard for a new comer to contribute to Checkstyle. 
The new comer have to take a lot of time to be familiar with checkstyle, which is quite hard and requires higher skills for the contributor.
This may block the new comer away from being an actual contributor. 

Secondly, the commit message of CheckStyle only contains the information of the issue number related to this commit. 
So, the developer cannot get any information of this commit from the message directly. It is harder for the developers to locate and analyze the bug.
Things get even worse if there is a long discussion in the issue/PR page in github, it is really difficult to find the true important information. 
Maybe CheckStyle should add some relevant important information in the commit message so the developers are able to get the required information more easily.
