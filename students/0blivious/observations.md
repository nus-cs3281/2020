## **Project**: [CheckStyle](https://github.com/checkstyle/checkstyle) 
Checkstyle is a tool for checking Java source code for adherence to a Code Standard or set of validation rules.

### Links
The link of the workflow of contributing to CheckStyle is [here](https://checkstyle.org/contributing.html#Content)

### Contributions made
* [Issue #7183: add JavadocMissingWhitespaceAfterAsteriskCheck](https://github.com/checkstyle/checkstyle/pull/7775)
* [minor: fix missed space violation from JavadocMissingWhitespaceAfterAsteriskCheck](https://github.com/checkstyle/checkstyle/pull/7883)
* [Issue #5832: add javadoc and xdoc example for LambdaParameterName](https://github.com/checkstyle/checkstyle/pull/7550)
* [Issue #5832: Add javadoc and xdoc Example for TypeName](https://github.com/checkstyle/checkstyle/pull/7525)
* [Issue #5832: add javadoc and xdoc Example for ParameterName](https://github.com/checkstyle/checkstyle/pull/7539)
* [Issue #5832: add javadoc and xdoc Example for StaticVariableName](https://github.com/checkstyle/checkstyle/pull/7530)

### Workflow
Below is the workflow for contributing to CheckStyle: 
1. Submit an issue and wait to be approved or choose an approved issue from the issue list.
2. Work on the issue and squash the changes to one commit.
3. Raise a PR and wait to be reviewed.
4. Edit your PR until being approved by all maintainers.

The workflow of CheckStyle is similar to RepoSense. The section listed some major difference between the projects.

#### Differences:

1. **Fast Response**: The developers of CheckStyle are very active and will ususally respond to PR within one day. Also, they have a very clear workflow by requesting approval in a certain series. The PR will only be merged after obtaining all approvals from requested developers.

1. **Issue Label**: They have a very complete set of issue labels. The 'approved' label is used to distinguish issue waiting for PR and issue for discussion. Contributors should only work for issue with the 'approved' label. While Reposense does have the 'todiscuss' label, it does not enforce it. This may cause difficulty for new contributors to find a issue to work on.

1. **CI Checks**: CheckStyle has in total 16 checks to pass before the PR can be merged. The tests covers a variety of aspects. They even have CI checks for commit message and number. Also, it requires the code to have 100% coverage using the Jacoco test report. CheckStyle also have a test named `pitest`, which is a kind of mutation test. It will modify some part of the code and expect the test to fail. If the code does not pass mutation test, possibly the test case or the main code can be improved.

1. **Regression Report**: CheckStyle has its own test tool and each time a new check is implemented, contributor is expected to submit a diff report which can displays the difference in terms of violation reported after introducing this new check. This can be very helpful for checking the effectiveness of the new code as well as determine the regression caused immediately.

### Suggestions to RepoSense 
For now, it seems RepoSense does not enfore a regression check before merging PR. Since most of our job now is dealing with the frontend, maybe we should have a more complete set of cypress test to detect any possible change in the frontend behavioiur.

We can also have a PR template to remind the new contributor to stick to our guidelines, especially the format the the line length constraints.

In addition, we should enfore a stricter rule in terms of reviewing sequence. Maybe we should even write this into our developer guide so that the new contributor will know who to seek help to. Also some contribution guidelines are not written explicitly in our developer guide such as the coding block for PR message and the 72 character rule.
