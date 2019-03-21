The particular project that I picked was part of a collection of firefox extensions. As such, they use many general libraries for rendering tooltips, popups, and interacting with the browser content.

These libraries are "imported" using the git submodule and any updates to the libraries can be easily updated through git as well. Using git submodules to manage libraries was new to me, and this was a concept that would be relevant for bigger projects with many moving parts.

However, this may not be so relevent for RepoSense. Even though the frontend report interface may be thought to be a separate component from the java backend which generates the report, they are too tightly related, the frontend having strong dependency with the format of the generated reports.

Another observation was the use of the `.editorconfig` file. The collection of firefox extensions is a rather large project with many different contributors. To help with the setting up of the development environment, this config file will handle code style such as indentation and trailing spaces. 

For projects with many different contributors this can be useful to automatically handle the different types of indentation styles. Since most editors respect the `.editorconfig` file, little has to be done to manage the file.

For RepoSense, this is something we could definitely do, using a `.editorconfig` to handle different kinds of code style. This is especially important for CLI based text editors such as vim where such options cannot be conviniently changed.

However, to tackle this issue, code style checkers such as eslint and checkstyle is used as part of the CI process to enforce a certain code style. The `.editorconfig` file can still come in useful for files where the style checkers miss (e.g. css files). With this configuration file, there would be less cases of early PRs having offending whitespaces changes.

Another useful thing to note is that most web based ide as offered by major code repository hosting platforms like github, gitlab and bitbucket do offer support for this config file. Therefore, this will make it more convenient for developers to work on their code, using these web ides.
