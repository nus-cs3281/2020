### Project: Ionic

[Ionic](https://ionicframework.com/) is the open-source mobile app development framework that makes it easy to build top quality native and progressive web apps with web technologies.

Ionic Framework is essentially a UI toolkit that consists of customized [Web Components](https://www.webcomponents.org/introduction) that achieve the same functionality as native mobile components on iOS and Android and mimic their look and feel. A comprehensive list of components available in Ionic Framework can be found [here](https://ionicframework.com/docs/components).

#### Documentations

The document outlining the contribution workflow can be found here: [CONTRIBUTING.md](https://github.com/ionic-team/ionic/blob/master/.github/CONTRIBUTING.md)

### My Contributions

Bug fixes:
- [fix(overlay): attach overlay element to document body](https://github.com/ionic-team/ionic/pull/20359)
- [fix(datetime): max property now works when hour, minute, or second set to 0](https://github.com/ionic-team/ionic/pull/20665)

New feature:
- [feat(datetime): add default value when picker opens](https://github.com/ionic-team/ionic/pull/20804)

### My Observations

The contributing workflow of Ionic is a standard one similar to other open-source projects. Since Ionic Framework consists of multiple packages (core, angular, react, and vue), all new issues submitted by the contributors are first labelled `triage`. One of the core developers then attends to the issue and label the issue with its package and type (bug or feature request).

Here are some observations made while contributing to Ionic:

- **Use CodePen to reproduce front-end bugs.** One advantage of Ionic being a front-end framework that works with VanillaJS, is the ease of testing and presenting the bugs. CodePen functions as an online code editor where developers can create code snippets and test them. To illustrate a bug of a particular Ionic component, contributors can simply paste the code that reproduces the bug in CodePen, and attach the script to Ionic's `js` and `css` files in the `<head>` section of HTML. CodePen then displays the rendered page side-by-side. Any changes made to the code segment also reflect in the rendered page in real time. Code segments on CodePen can be saved and shared with links. Hence, it is recommended to include a link to the code segment that presents the bug for easy verification and assessment of the bug by other contributors.

- **Use bot created by GitHub App to manage issues.** All the issues submitted by contributors will first be labelled `triage` automatically by the `ionitron-bot` which manages the issues. It highlights the new issues to the core developers so that they are not easily missed and prompts further actions from the core developers, such as categorizing the issue or seeking for clarification. The bot also automates closing and locking issues that are not following the provided issue template, not within the scope (support type / "how to" questions), or with an inactive conversation for weeks. It also automatically provides a message to the contributor while closing the issue, saving the need for core developers to repeat same instructions for many times. With the bot, the core developers can spend their time on more important issues. This can possibly be adopted by TEAMMATES if the number of contributors and issues grows. 

- **Make constant releases.** As an open-source front-end framework that is used by many projects, Ionic makes constant releases to deliver bug fixes as soon as possible. The intervals between releases are not fixed; depending on the importance and urgency of bug fixes, the intervals range from two weeks to one day. Moreover, there is a clear distinction between releases involving bug fixes and new features. Patch releases (version number changes by `0.0.1`) only contain bug fixes while minor releases (version number changes by `0.1.0`) contain both bug fixes and new features. Major releases (version number changes by `1.0.0`) contain breaking changes and are preceded by beta releases (`X.X.X-beta.X`). These clear distinctions ensure that developers using Ionic will not easily introduce new behaviors or breaking changes while upgrading the framework.

- **Do screenshot tests.** Since Ionic is a front-end framework, it is important that a PR should not introduce changes to a component's look and behavior when it is not supposed to. With the aforementioned bot, screenshot checks are carried out to compare the look of components before and after the changes made in the PR, pixel by pixel. It automatically takes more than one thousand screenshots and highlights to the contributor any mismatched screenshots after comparison. The drawback of this test is that it needs extra computational resources and is very time-consuming. A complete round of screenshot test takes about 8 days to finish. Hence, only PRs made by core developers can trigger screenshot tests.
 