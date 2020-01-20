# Project 2019-2020

The goal of the project is to develop an application and apply during its development, a selection of the techniques studied in the classes.
The deadline to deliver the project will be on **February 28th 23:59 PM CET**.

## The application

The application to develop is a command line tool to compress and decompress a given binary file. The file will be provided either as a parameter from the terminal or in the standard input of the program. The tool should be designed to compress only one file. The user must be able to choose between, at least, two different compression algorithms. Users should also be able to decompress a given file compressed before with the same application. In this case, the tool should automatically know which decompression algorithm to use to obtain the original uncompressed file.

The application can be developed in any programming language. Students must design how the application will receive commands and parameters from the terminal, that is:
- The path of the file to compress/decompress or if the program should use the standard input
- The compression algorithm to use
- Whether the file should be compressed or not
- Get a help message with the information about the parameters and options

### Compression algorithms

The application should provide, at least, two different compression algorithms. Any additional compression algorithm implemented will be considered as an extra action for the project and will receive a bonus.

We recommend the two following compression algorithms:

- [Huffman coding](https://en.wikipedia.org/wiki/Huffman_coding)
- [Lempel-Ziv-Welch algorithm]()

Both are well known algorithms and students may find plenty of information and even implementations online. However, students must provide their own implementations.

## The evaluation

Each group should provide a repository, either in Github, Gitlab or using the Gitlab instance from ISTIC. The repository may be private or public but it should be visible for the teachers so it can be evaluated.

The development history will be a strong point in the evaluation. All students in the group must collaborate with the development and the history should reflect this. Therefore, each student should use his/her own account.

In order to be evaluated a project **must** comply with the following conditions:

- Have a unit test suite
- The unit test suite should be executed automatically in a Continuous Integration (CI) server after each commit and report back the result
- The CI execution should also monitor the code coverage of the test suite and report it back. The final test suite must achieve at least a 60% coverage.

CI integration can be achieved in Github using [Github Actions](https://github.com/features/actions) or well known CI solutions like [Travis](https://travis-ci.org/) and [Jenkins](https://jenkins.io/). These solutions can be also used with Gitlab and Gitlab also provides its own solution for [CI integration](https://docs.gitlab.com/ee/ci/).


In order to improve their grade, students must incorporate the following techniques:

- Static testing/analysis. Using tools like PMD, FindBugs and alike that we saw in classes.
- Mutation testing/analysis.
- Fuzzing

There are three ways to incorporate these techniques into the project:
- Use the techniques manually and take actions upon their feedback.
- Automatically execute these techniques and automatically incorporate the feedback into the project. For example, run PMD after every commit and for each issue signaled by PMD automatically create an issue in the issue tracker. Students may use the existing tools and should configure and adapt them to their needs and criteria.
- The students create their tools implementing these techniques and integrate them in the CI with automatic feedback.

The development history should reflect the actions taken given the feedback from these techniques. For example, each PMD finding that deserves a solution should be reflected in an issue and at some point a commit should contain code to solve the issue.

The number of techniques incorporated to the development of the project will be reflected in the grade (the more the better). The degree of complexity in the integration will also be reflected (the more automatic, the better).

Any other form of integration and any other technique integrated will be considered as an extra action. All extra actions will be granted a bonus.

### The report

Each repository should contain a report that documents the development of the application and how the testing techniques were used. The report should also include the problems students found during the development of the project and how they were solved. It should also contain a description of the problems students may not have solved. The quality of the report will be reflected in the final grade.

The report must be written in Markdown and all files conforming the report should be included in the repository

### The deadline

On **February 28th 23:59 PM CET** all repositories will be cloned and that will be the version to use for the evaluation of the project. The evaluation will consider the development history of the repository, the report and all the information that can be extracted from Github, Gitlab and all integrated tools.
