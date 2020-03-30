### Projects: Pylint & Checkstyle

Both Pylint and Checkstyle are static code analysis tools (for Python
and Java programs respectively). Both tools are mature and well-known in the communities of their respective
languages. Pylint has 370 checks available by default, with a project history
spanning 17 years. Checkstyle has 170 checks available by default, and has been
under development for 19 years.

Interestingly, though Python is a dynamically typed language, Pylint can perform
some type checking as well.

Links to documents for new contributors:
- [Pylint's guide for new contributors](http://pylint.pycqa.org/en/latest/development_guide/contribute.html) and [the technical reference, which gives an overview of the project architecture](http://pylint.pycqa.org/en/latest/technical_reference/index.html#technical-reference)
- [Pylint's guide for adding new checks](http://pylint.pycqa.org/en/latest/how_tos/custom_checkers.html)
- [Checkstyle's guide for new contributors](https://checkstyle.org/contributing.html)
- [Checkstyle's guide for adding a new check](https://checkstyle.sourceforge.io/writingchecks.html)

### My Contributions

I added 2 new checks to Pylint, and a new command to the Pylint CLI tool.
These contributions will be part of Pylint version 2.5.

Links to PRs:
- [Added a new check that detects incorrect usages of Python's `assert`
  statement](https://github.com/PyCQA/pylint/pull/3346)
- [Added a new check that typechecks the arguments of an `isinstance` function
  application](https://github.com/PyCQA/pylint/pull/3404)
- [Added a command that lists all extensions available in the Pylint CLI
  tool](https://github.com/PyCQA/pylint/pull/3366) - Note: the project maintainer merged my branch **from the CLI**
  (as compared with merging via GitHub). Hence, the PR has been closed though
  the contribution was merged.
  [**Here is the commit**](https://github.com/PyCQA/pylint/commit/d3409000808faf3198597aa638c9c60e041a421a) showing my merged contribution.

For Checkstyle, I wrote documentation to illustrate the usage of a check.

Link to PR:
- [Add documentation examples for
  InnerAssignmentCheck](https://github.com/checkstyle/checkstyle/pull/7796)


### My Observations

#### Automating "administrative work" saves time

Checkstyle has a comprehensive suite of continuous integration checks, that
automates many administrative tasks. For example, their CI scripts can detect
the following (amongst others):
- whether the PR description contains a reference to the Issue being fixed ([link to Travis
  script](https://github.com/checkstyle/checkstyle/blob/master/.ci/travis/xtr_pr-description.sh))
- whether the PR branch is too far behind the master branch ([link to Travis
  script](https://github.com/checkstyle/checkstyle/blob/master/.ci/travis/travis.sh#L201-L223))
- whether the PR is fixing an issue that has not been approved yet ([link to
  Travis
  script](https://github.com/checkstyle/checkstyle/blob/master/.ci/travis/xtr_pr-description.sh))
- if there is a typo in documentation (using [this spellchecking
  tool](https://github.com/jsoref/spelling))

With these checks, reviewers need not spend time catching violations of project
conventions. They can focus on the actual review instead.

**Recommendation for RepoSense**

We should try to automate the "admin work" as far as possible.
This process has been started as we have been investigating how GitHub actions
can be applied (to close stale PRs, for example).

In addition, we can use a git hook to run the linters before every `git push`
command is executed. This removes the need for reviewers to remind PR authors
that the CI checks are failing due to a code style issue. We could also consider
adopting the automated spell checker used by Checkstyle.

#### Attracting new members by setting aside meaningful work for them

Given that open source projects (like those under NUS OSS) are often developed
by volunteers, it's in the interest of projects to attract new members.

Both Pylint and Checkstyle attract a steady stream of new contributors.

One reason is that the maintainers use triaging to higlight areas where *new* contributors can
**realistically make meaningful contributions**. On Pylint's issue tracker,
several interesting (and realistic) ideas for new checks are set aside
for new contributors. In Checkstyle's case, maintainers mark out not only "good
first issues", but also "good second issues" and "good third issues". Such
triaging makes it more likely for new members to invest time on the project,
because they see a clear pathway towards making a significant impact.

**Recommendation for RepoSense**:
RepoSense does not have a high number of **meaningful** first-timer issues.
We should consider brainstorming more such issues, especially in the periods when
we are expecting new contributors.

Moreover, it can be confusing for new contributors to find a suitable task
after making their first contribution. There could be
an additional `Easy` label that identifies work for developers who have
made *some* first contribution, but are still new to the project. There
shouldn't be any restriction on the number of `Easy` issues one can fix.

With the `Easy` label and a larger number of first-timer issues, new
contributors are more likely to invest time in RepoSense as they will see a
clear pathway towards a meaningful contribution.

#### Comprehensive commit messages make the project more accessible for new members

When we implement a feature or fix a bug, there are often multiple possible
solutions. Ultimately, we make a decision based on the team's judgement.
However, the reasons for these technical decisions can become inaccessible to new
members if they are not documented anywhere.

After working on Pylint, I have come to appreciate RepoSense's comprehensive
commit messages. It is incredibly convenient that I can understand the evolution
of most classes and methods by retrieving the commits associated with them.

**Recommendation for RepoSense**

Though RepoSense has strict conventions for commits on `master`,
there are no conventions enforced for commits in PR branches.

I suggest that we should adopt the use of `git rebase` (and not `git merge`)
for bringing PR branches up to date with `master`.
This will remove a significant amount of "noise" from merge commits in the PR branch.
