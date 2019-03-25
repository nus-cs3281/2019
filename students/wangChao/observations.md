The external project that I picked is CheckStyle, which is a tool for checking Java source code for adherence to a Code
Standard or set of validation rules (best practices).

The link of the workflow of contributing to CheckStyle is [here](https://checkstyle.org/contributing.html#Content)

The basic workflow is like this: 
1. Submit an issue and wait to be approved or choose an approved issue from the issue list.
2. Work on the issue and squash the changes to one commit.
3. Raise a PR and wait to be reviewed.
4. Edit your PR until being approved by all maintainers.

The workflow of CheckStyle do not have a big difference with RepoSense and SE-EDU.

There are two impressive aspect when I contributes to CheckStyle. One is CI Test, another is Diff Report.

For the CI Test, CheckStyle has 17 checks to pass in order to proceeded with PR. The tests covers a variety of aspects.
For example, it ensures that the project is able to run on all JDK version and all Platforms. Also, it requires the 
code to have 100% coverage. 100% is even not enough for the tests. CheckStyle also have a test named `pitest`, which is
a kind of mutation test. It is basically modifying the test code to look for tests failure. It will find out the lines 
that are able to be modified without tests failure, which indicates either the test case can be improved or the main code
can be improved.

For now, RepoSense do not have a coverage test yet, which may because the test coverage is not satisfying at the early 
stage of RepoSense. Now, we already have a high code coverage, so the previous concern is not true anymore. Also, having 
a coverage test allows us to improve our testing with higher revenue and lower costs. So, maybe RepoSense should integrate 
coverage test now.

Currently, AB4 has coverage test. However, it do not have mutation test. As a project that teaches students about SE 
related knowledge. Maybe we can integrate mutation test in our code because it is reasonable to let the students know
that there is another kind of test to test code quality.

For Diff Report, basically, it ask all the changes related to main code that may cause a regression to generate a diff 
report, which compares the result of analysis generated for a large number of public repos before the change and after 
the change. This process is to ensure that no regression happens after the change.

Because AB4 is not analysis based application, so Diff Report is not suitable for AB4. 

For RepoSense, we already have a Netlify preview for some Repos which plays a similar row. However, it is not same.
Maybe we can add a tool that are able to analyze the difference of the two report generated so we can have a better 
insight of potential regressions.
