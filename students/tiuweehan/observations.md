### Project: Netlify CMS

[Netlify CMS](https://www.netlifycms.org/) is an open source content management system that enables developers to provide editors with a friendly UI and intuitive workflows. It can be used with any static site generator to create faster, more flexible web projects. Content is stored in the developer's Git repository alongside the code for easier versioning, multi-channel publishing, and the option to handle content updates directly in Git.

I chose Netlfiy CMS as my external project as it aims to be a core feature within the [JAMStack](https://jamstack.org/), an up and coming tech stack that delivers fast and secure sites and apps by pre-rendering files and serving them directly from a CDN, removing the requirement to manage or run web servers.

### My Contributions

#### Enhancement: Add support for multiple languages

I helped to add support for different languages within the application and some external widgets using the [React Polyglot](https://www.npmjs.com/package/react-polyglot) library. This was particularly difficult as the application uses a single source of truth for the different locales within the core component, but also had to be referenced by the external widgets. I managed to figure out how the widgets were integrated into the core component and subsequently how to pass the references over. As proof that it works, I also added several screenshots and translations to the PRs.

Relevant PRs:
- [fix(locale): remove hard coded strings #3193](https://github.com/netlify/netlify-cms/pull/3193)
- [fix(locale): remove hard coded string literals #3333](https://github.com/netlify/netlify-cms/pull/3333)

#### Enhancement: Bug Fixes

I fixed a bug that resulted in a mismatch between the documentation and the implementation regarding the media library usage for `uploadcare` and `cloudinary`.

Relevant PRs:
- [docs: fix media library usage #3181](https://github.com/netlify/netlify-cms/pull/3181)

### My Observations

#### External Project Workflow

Netlify CMS has documentation page on contribution and development guidelines. They utilise a [forking workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow) and [feature branches](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). Contributors are required to rebase on master when opening a Pull Request and before merging in a Pull Request. Pull Requests are reviewed by at least two maintainers prior to merging. There is also a community slack channel and forums to allow new developers to chat with maintainers and see what are some of the issues being actively discussed.


#### Well-documented Contributing Guide

The contributing guidelines are well-documented. It includes comprehensive guides for setting up, testing, linting, hot-reloading and making Pull Requests. It was easy for myself as a newcomer to get started with the project. I particularly liked that the Netlify CMS community is very encouraging towards new contributors. To quote parts of their documentation: 
- "Contributions are always welcome, no matter how large or small."
- "If you need help with Git or our workflow, please ask in our community chat. We want your contributions even if you're just learning Git. Our maintainers are happy to help!"
I think that it is reassuring especially for beginners who may not be confident in tackling large codebases.

Relevant Links:
- [Contributing to Netlify CMS](https://github.com/netlify/netlify-cms/blob/master/CONTRIBUTING.md)
- [Development Rules & Guidelines](https://github.com/netlify/netlify-cms/blob/master/website/README.md)
- [Slack Channel](https://netlifycms.slack.com/join/shared_invite/enQtODE1NTcxODA5Mjg1LTRjYWExM2MyZDJmODA3YmVkMjI2YmQwZDg2ZDUyYTMyM2Y3Zjc1ZTJhNDBkYmMwNjA2ZTkwODY4YjZjNGNlNTE)
- [Community Forums](https://community.netlify.com/c/netlify-cms)

#### Slack and Forum for Discussion

Netlify CMS has a public Slack group for discussions with dedicated channels for both users of Netlify CMS as well as developers. This makes it easy for new developers to understand the issues that users are facing as well as ongoing discussions within the developer community. New contributors can also join discussions and chat with the maintainers directly if they need help on issues they are working on.

### Suggestions for Internal Project

1. Much like Netlify CMS, TEAMMATES could benefit from having a community slack channel to reach out to a larger pool of new developers. Currently, TEAMMATES relies on the use of 'Good First Issues' for newcomers to contribute the project, but they are not frequently raised. The nature of GitHub issues also may not be conducive for general discussions as compared to the responsive nature of Slack channels. Having a community slack channel allows new developers to approach and speak directly to current maintainers to look for issues or seek help on issues that they are working on.

2. A good practice that Netlify CMS adopts is to enforce style guidelines on Git commits through the use of pre-commit and pre-push hooks with Husky. This results in a more consistent set of commit messages and makes it manageable for developers to read past changes.

3. Another common issue I observed in TEAMMATES is that developers sometimes forget to lint or run regressions tests before pushing onto GitHub, thus failing the CI and requiring separate commits to fix these trivial issues. Pre-push hooks could likewise also be implemented to enforce linting and testing before a developer pushes to GitHub.
