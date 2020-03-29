### Project: [Gatsby](https://www.gatsbyjs.org/)

Gatsby is a free and open source framework based on React that helps developers build blazing fast websites and apps. Some of its main selling points are:

- It is fast because it comes with many [performance optimizations built-in](https://www.gatsbyjs.org/blog/2017-09-13-why-is-gatsby-so-fast/).
- It is easy to get started with because it has [hundreds of pre-built templates called "starters"](https://www.gatsbyjs.org/starters/?v=2).
- It has a [flexible and robust data layer powered by GraphQL](https://www.gatsbyjs.org/docs/content-and-data/) that allows developers to build ambitious static sites from dynamic data.

Gatsby also provides [a set of contributor guides](https://www.gatsbyjs.org/contributing/how-to-contribute/) that I found very useful when trying to contribute to the project.

### My Contributions

- [Allow graphiql to set initial query variables from query string](https://github.com/gatsbyjs/gatsby/pull/21158)
- [Split up gatsby-node](https://github.com/gatsbyjs/gatsby/pull/21217)
- [Migrate eslint-config to TypeScript](https://github.com/gatsbyjs/gatsby/pull/22294)
- [Incorrect PackageJson type](https://github.com/gatsbyjs/gatsby/pull/22406)
- [Migrate gatsby-dependents to TypeScript](https://github.com/gatsbyjs/gatsby/pull/22422)

Initially, I familiarized myself with the Gatsby codebase by fixing a bug in the GraphiQL inspector. Once I was familiar with the project, I started to take up larger issues like refactoring `gatsby-node` into a set of well-structured utilities categorized by their function. I also contributed to their ongoing TypeScript migration, helping to migrate some of their source files and fixing some incorrect types.

### My Observations

These are some positive things that I've observed as a contributor on Gatsby.

1. **[A comprehensive set of procedures](https://www.gatsbyjs.org/contributing/how-to-contribute/)**

   Most open source projects have contributor guidelines that describe how contributors can help out and Gatsby is no different. However, Gatsby maintains the contributor guidelines as part of a larger set of documentation that describes their operating procedures at every step of the process. This set of documentation includes everything from filing/triaging issues and managing pull requests, to documentation and code guidelines, to even non-technical topics such as how one can contribute to the Gatsby community with blog posts, talks, workshops and more.

   This comprehensive set of procedures helped me understand their workflow as well as what I was expecting to happen next. For example, by reading the document on [managing pull requests](https://www.gatsbyjs.org/contributing/managing-pull-requests), I was able to understand exactly who had the rights to review and merge my PR. This made the process very transparent and clear by removing any sort of guesswork.

2. **A focus on building the community**

   After my first PR was merged into Gatsby, I was added into the Gatsby organization on GitHub. This caught me by surprise because large open source projects usually only add core contributors into their organizations. I soon realized that Gatsby automatically adds anyone who has merged a PR, and that the organization contained [almost 3000 people](https://github.com/orgs/gatsbyjs/people). Anyone in the organization can review PRs, but only people in the `gatsby/core` and `gatsby/learning` teams can merge PRs.

   By automatically adding all contributors into the organization, Gatsby has managed to build a community around its product. There is an internal discussion board where the core team and contributors talk about ideas on how to improve Gatsby and I think this is a great initiative. Gatsby also uses a Discord channel to facilitate discussions.

   Also, as part of the organization, contributors also get to have the Gatsby badge on their GitHub profile which is always nice.

3. **Incentives for contributors**

   This idea is probably not feasible for all open source projects because it requires some financial capacity but Gatsby has a reward system for contributors. Gatsby has its own [merchandise store](https://store.gatsbyjs.org/) where they sell some project-related items. For Gatsby contributors, 1 merged PR earns you any $10 item for free, and 5 merged PRs earns you any $26 item.

   When my first PR was merged, Gatsbot (Gatsby's GitHub bot) [notified me](https://github.com/gatsbyjs/gatsby/pull/21158#issuecomment-582594988) that I qualified for something from their store which was a pleasant surprise. This ties in with Gatsby's overall emphasis of building a community around the product by building a sense of identity through their merchandise. This is also probably good publicity for Gatsby as it increases the likelihood of contributors talking to others about the product.

4. **Using `CODEOWNERS`**

   Gatsby has several teams that manage different parts of the project. They use a [`CODEOWNERS` file](https://github.com/gatsbyjs/gatsby/blob/master/CODEOWNERS) to map parts of the project to their respective "owner" teams. By doing so, new PRs opened will automatically have their changed files matched against the `CODEOWNERS` file and a review will be automatically requested from the team responsible. This ensures that PRs are reviewed promptly and that no PRs get lost in Gatsby's busy PR tracker.

### Suggestions for internal projects

Since I'm working on the TEAMMATES team, I've come up with some things that could be adapted from Gatsby. For the most part, TEAMMATES already adopts most of what Gatsby does.

1. If we have the financial means to, perhaps we can consider incentivizing contributors in some way. Gatsby is well-funded so they can offer expensive things like T-shirts and hoodies but there are more affordable options like stickers. From what I've seen in open source projects, people are always happy to receive some kind of acknowledgement for their contributions, even if it's something small like stickers. This would also be good publicity and would increase the visibility of the TEAMMATES project in the long run.

2. We can consider implementing a `CODEOWNERS` file, but it might be slightly challenging because we don't really have clear separation of "owners" in the project. Still worth exploring if we're interested in assigning this type of responsibility in the future.
