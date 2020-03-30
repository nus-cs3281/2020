### Project: OpenDota

OpenDota is a fully automated [Dota 2](https://dota2.com) match replay parsing tool that provides the [OpenDota API](https://docs.opendota.com/) for consumption, which in turn powers the [OpenDota UI](https://www.opendota.com/).

### My Contributions

I added 2 new features to OpenDota. 1 for the web UI, and the other for aggregating data to expose through a new endpoint.

I have merged 2 PRs for OpenDota:
- [Item popularity endpoint](https://github.com/odota/core/pull/2116)
- [Show items bought in player matches page](https://github.com/odota/web/pull/2462)

### My Observations

1. **Meaningful first issue**: A meaningful first issue is important as it is the first guide into the codebase of a project. My first issue in OpenDota was highly educational, as the issue was not contained in a small area. I had to consider multiple parts of the project, such as gaining knowledge of the backend API of the project.

2. **Fast response rate**: My reviewers are highly responsive in giving reviews and feedback in my pull request, allowing contributors to quickly iterate on the pull request. Also, they were quick to provide extra help with the project on Discord, such as answering queries in getting started with the project and other relatively basic questions.

3. **Quick setup**: OpenDota uses docker with microservices to ensure that a single point of failure would not bring down the entire server. More importantly for me as a new contributor, Docker allowed me to get started quickly, with minor issues that were resolved quickly. Otherwise, there would be a lot of steps required to get the service up, such as manually running several scripts for each service.

### Suggestions for internal projects

My internal project is Reposense, and they are both quite similar in the regard that they both have a frontend and a backend service, just that OpenDota is more complex in nature.

1. **Wider scope for first issues**: I personally find the labelled good first issues to be rather self-contained. While it is easy to resolve these type of problems, they don't actually teach the contributor much about the project. I feel that a good first issue should be a stepping board for new contributors to understand more about the project, rather than simply fixing a minor bug with no exposure to the rest of the project. With that said, I don't think the issue should span the entire scope of the project, but should at least cover a sizable amount of the codebase.


2. **Setup public chat channel**: I find that while the internal contributors have a slack channel to communicate our problems and ask for help, external contributors do not have this avenue to ask for help. I feel that we can setup a public chat channel to ease external contributors in contributing to the project, as well as answer any queries that our documentations may not cover.
