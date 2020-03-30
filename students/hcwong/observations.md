### Project: Hugo

Hugo is a widely used static site generator written in Go, with over 40.7k stars on Github. It claims to be the fastest static site generator. At its most basic functionality, it can transform Markdown, HTML, CSS files into a static site easily when combined with other tools like Netlify. However, unlike other simpler static site generators, Hugo also boasts complex content management and great built-in templates for users to use.

I took up this project as I wanted to learn more about Golang instead of doing my usual JavaScript stuff.

### My Contributions

#### Enhancements

[Allow raw string literals in shortcode params](https://github.com/gohugoio/hugo/pull/6753/)

Hugo has a great feature called [shortcodes](https://gohugo.io/variables/shortcodes/#readout) that allow for Hugo Pages to contain variables. These variables can also take in "parameters" of sort, adding to their overall usefulness. 
I helped to add support for escaped quotes and Golang raw strings in this PR for such parameters. I found this to be technically challenges as I had to delve into the lexer code and understand how it parsed these parameters out. In fact, the lexer 
in Hugo is based on a great [talk](https://talks.golang.org/2011/lex.slide#1) given by one of the Golang coreteam members.

[Add hugo.IsProduction shortcut](https://github.com/gohugoio/hugo/pull/6953)

Hugo offers conditionals to selectively render certain parts of the markdown file. I added a shortcut for a commonly used conditional.

#### Bug fixes

[Add support for newline in raw string shortcode](https://github.com/gohugoio/hugo/pull/6771)

This is a bug fix which helped to add support for newline characters in raw string shortcode parameters.

### Contributions

Like most other open source projects, Hugo works off a fork and branch model. Users fork the Hugo repository and make their changes on their a branch of their fork,
before sending the finished pull request back to the main repository. As Hugo is maintained only by a few developers, only one approver is needed before the PR is squashed and merged.

Hugo also does releases fairly often, so it will not take long before a new contribution 

- [Contribution Guide](https://github.com/gohugoio/hugo/blob/master/CONTRIBUTING.md)
- [Contributing to documentation](https://gohugo.io/contribute/documentation/)

### My Observations

I've enjoyed working with the Hugo codebase, in no doubt due to the following few features.

1. A great and responsive community

Hugo's creator and chief maintainer, bep, does a great job responding to new issues and PR fixes. All my PRs were reviewed within 3 days. This responsiveness 
enables contributors to contribute more effectively, as they are able to quickly follow up with fixes while the context of the PR is still fresh in their mind. 
However, more importantly, Hugo also has their own forum, where its many users can ask questions and get fellow Hugo users, or maintainers to help answer it. The forum is fairly active and is very friendly and welcoming to newcomers, making it an effective way to integrate new users and developers. In fact, Hugo's Github Issue tracker is used primarily for proposing enhancements or formalizing bug reports. This also reduces the burden on maintainers and developers, especially since Hugo is not supported by big companies, unlike projects like React.

2. Great external documentation

All of Hugo's features have great documetation that is updated and easily accessible on its [website](https://gohugo.io/documentation/). This sets it apart from its counterparts as users are able to better understand to power and functionality that Hugo offers, hence increasing adoption. All PRs to Hugo that change functionality must also update the documentation whenever necessary, thus helping it to maintain documentation quality.

3. Easy setup process

Sometimes, when faced with a huge project, I sometimes get intimidated by its size and do not even bother setting up to see if I can contribute to it. However, with Hugo, there is a great contributing guide for newcomers that details how to set up the process from scratch, and even offers help on some basic Git functionality. This thorough guide helps to reduce bugs while setting up and enables more people to contribute. The guide is given above under the Contributions section. This ease of setup is also in part attributed to the nature of Golang, which focuses a lot on simplicity.

However, I have also encountered some difficulties while contributing to this project. In particular, Hugo does not have much code level documentation for developers. The bulk of commits are done by the small team of maintainers, who are very familiar with the codebase.  As a new developer, I often had to use the external documentation for users to try and locate, and then understand the code. As Hugo is also a fairly large project, developers who are new to the project may have to follow multiple call stacks in order to figure out where to make their change. Also, some of the variables used are quite similar, which can further confuse the developer. To help ease new developers, one point for improvement could be to maybe insert a few markdown files at each top level folder to explain what the code inside does and the functionality they support. This will go a long way in helping new contributors make changes effectively and quickly.

### Learning Point for TEAMMATES.

TEAMMATES and Hugo have similar review processes, including the need for PRs to be approved and for CI checks to pass. I think the key thing TEAMMATES could learn from Hugo is not related to the code, but more of the documentation and community. I think that TEAMMATES does not effectively retain developers, in that people contribute and then leave permanently. When they do so, we lose their expertise and insight. Code that they contributed may also be more difficult to maintain. The same cannot be said about Hugo. Even though it is a few weeks since my last contribution, I still get an automated email from the forum informing me of new posts, thus helping to keep me engaged.

As a school/student-run repository, TEAMMATES may not have the resources or time to setup such a complex forum. However, what we could do could be to setup a simple Telegram Chat, or Slack channel where developers can ask questions quickly without the hassle of raising a Github Issue. This is also important as it seems that many of our one-time contributors are students, and Slack and Telegram are widely used by this demographic. The Slack channel will also enable maintainers to quickly onboard new developers, as we may not check Github that often.

Another thing we could learn would be the excellent documentation. TEAMMATES actually has a good developer guide, however, it is not frequently updated, and a good deal of issues on our Issue Tracker are related to setting up. The documentation for setting up could be reviewed and expanded to cover different OSs and even expand the FAQ section when we spot common bugs occuring. This way, we can get more people to contribute to the project.

