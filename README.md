# Cox Automotive / Manheim Release Engineering Hiring Project

Manheim's Release Engineering (RE) team develops tools, libraries, documentation, and processes to allow the seventy-plus autonomous development teams that we support to do their jobs faster and more efficiently, reliably, and securely. Each of the teams that we support is autonomous and has full control over the choice of languages and tools that they use; when they choose ours, it's because we provided the most compelling solution. When we do our jobs well, our products are also adopted by some of the hundreds of Cox Automotive development teams outside of the Manheim business unit.

We don't do whiteboarding, programming exercises, etc. in our interviews; our interviews are a conversation about you, about us and our company, about your experience, and about how well we think you'd be a fit for us and vice-versa. This project is intended as a minimal way for you to show us your technical skills in a self-paced, low-pressure fashion (i.e. something akin to the real work you'd be doing here).

This project is intended to take no more than a few hours to complete; our interview process is generally a fifteen- to twenty-minute phone screen and two hours in person or over video, so think of this project as rounding out the time expected of a more in-depth interview.

__Note:__ This project is brand new as of April 2019. If you have any questions, feel free to ask us. If you find yourself working on this for an unreasonable amount of time (we'd suggest six hours as the absolute maximum limit), please submit what work you've done up to that point along with some ideas on what we should change to make this project fit a reasonable amount of time.

## Scenario

Our business unit has just formed a brand new development team, the Insights Team, tasked with developing data visualization tools for executive leadership. Their first task is to develop a simple dashboard app, but they'll likely be developing dozens of other similar small applications in the future. The project is highly visible, so they want to work as fast as possible, and their goal is a fully-automated CI/CD system for their apps. They don't have code ready yet but want to deploy as quickly as possible once they do.

You've been tasked with working with<sup>[1](#footnote1)</sup><a name="reference1"></a> the Insights Team to develop deployment tooling for their Dashboard app. Your goal is to write deployment tooling for their app so that once the team is ready to start writing code, they have a working base already in place and can jump into their CI/CD workflow. Once you're done with the work ownership of the deployment tooling will be handed over to the team, and they hope to also use your tooling as a pattern for their future applications, so clarity and maintainability matter.

Since the team doesn't have code ready yet, you should use a simple / example "Hello World" application. This will act as a placeholder for the team's code (when ready), which you can assume will be a bit more involved than Hello World (i.e. it will probably persist data somehow, and will definitely read data from various datastores).

## Your Task

Your task is to provide tooling for deployment of the Dashboard App. The team is leaning towards Jenkins for CI/CD but isn't completely decided yet, so you'll need to provide some commands or scripts along with instructions for how to run them. The team will execute them locally until they're decided on CI/CD, and then will execute the same commands/scripts from within their CI/CD system. You can assume that someone on the team has basic knowledge of the tooling for their language, but your instructions should be complete and clear.

We want to find out how well you know what _you_ know, not what _we_ know. As such, you'll need to find a "Hello World" web application to use; feel free to choose one written in whatever language you're most comfortable with. We've provided some [examples](hello-world-examples.md) to speed up the process, so you won't have to write this yourself.

We primarily use AWS, so if you're familiar with AWS and have an account to test with, that would be great! If not, no worries! We'd prefer if your code deploy to a public cloud provider that offers accounts with a "free tier" (so that we can run your code without incurring any additional cost). If that's not within your area of expertise, feel free to use whatever you think would be easiest for one of us to run on our laptop.

The Dashboard App will have at least non-production and production environments, and may have additional environments (such as User Acceptance Testing) in the future, so your code should support this. Configuration information (such as account, VPC, and subnet information if deploying to AWS) should be manually specified by the user in your initial version, but you can expect this to come from some sort of external data source once the team moves to their CI/CD environment. You should also provide tooling to completely destroy / tear down everything that was created for a given environment.

This is intended to be an internal, non-business-critical application, but visible to many internal users. Your deployment plans should reflect that.

Please remember that the goal of this is to allow us to see your technical and decision-making skills and thought process in a relatively low-stress, self-paced way. While we're certainly looking for code quality, this doesn't need to be "perfect". Also keep in mind that the hypothetical team developing this application may not have much experience with the platform it's deployed to, so keeping things simple and clear is good.

Finally, don't reinvent the wheel. Use whatever resources you can, including existing relevant code if you have it.

## Getting Started

The process described below relies on ``git`` and GitHub. If you don't have a GitHub account or aren't familiar with git at all, that's fine. We use it a lot here, but as with all skills, you can always pick up a skill as needed. Some links are provided below if you're not familiar with git.

1. Get this repository as a starting point:
   * If you have a GitHub account and you're comfortable making your submission public, [fork](https://help.github.com/en/articles/fork-a-repo) this [repository](https://github.com/manheim/re-hiring-project)
   * If you have a GitHub account but you're not comfortable making your submission public, you can [duplicate](https://help.github.com/en/articles/duplicating-a-repository) this repository to a new private repository of your own.
   * If you don't have a GitHub account or want to ensure that your work on this stays as private as possible, you can clone this repository with ``git clone https://github.com/manheim/re-hiring-project.git`` and do all of your work with it locally / offline.
2. Replace this ``README.md`` file with one specific to your code.
3. Write your code and the README to accomplish the above-described scenario and task. We're especially interested in seeing your methodology and thought process, so please ``commit`` often and please don't squash any commits.
4. Submit your work to us:
   * If you created a public fork of this repository on GitHub, you'll just need to let us know your GitHub username.
   * If you created a private fork, you'll need to let us know your username and also add at least one of the [contributors on this repo](https://github.com/manheim/re-hiring-project/graphs/contributors) as a [collaborator on your private fork](https://help.github.com/en/articles/inviting-collaborators-to-a-personal-repository).
   * If you only cloned the repository locally, or if you don't want to add collaborators to your private fork, please send us a gzipped tarball (``.tar.gz`` or ``.tgz``) of your complete local clone, including the ``.git`` directory.
5. Optionally, but greatly desired, is if you also provide us with an idea of how long it took to complete this project and any other suggestions you have for improvement of it, or other feedback. This information will _not_ be used in evaluating your submission but will be used for improving this project in the future. After all, we're strong believers in iterative development, continuous improvement, and measuring as much as we can.

### Git Resources

For this project, the only things you should _need_ to do with git are ``git clone``, ``git add``, and ``git commit`` (and, if you used the GitHub fork method, ``git push``). Roger Dudler has a simple and concise guide for getting started with git at [https://rogerdudler.github.io/git-guide/](https://rogerdudler.github.io/git-guide/), which should cover the basics that you need to complete this project.

If you're not familiar with git and would like to learn a bit more about it, here is a selection of resources that we found, we've used in the past, or were recommended to us:

* [git/github guide - a minimal tutorial](https://kbroman.org/github_tutorial/)
* [Tutorial: Git for Absolutely Everyone - The New Stack](https://thenewstack.io/tutorial-git-for-absolutely-everyone/)
* [Resources to learn Git - try.github.io](https://try.github.io/)
* [Git Immersion](http://gitimmersion.com/) - "A guided tour that walks through the fundamentals of Git, inspired by the premise that to know a thing is to do it."
* [Git Tutorial | Backlog](https://backlog.com/git-tutorial/)
* [Git - gittutorial Documentation](https://git-scm.com/docs/gittutorial)

## Footnotes

<a name="footnote1">[1](#reference1)</a>: This scenario is slightly contrived, as in reality we have many established tools, libraries, and patterns for this problem area. Our team also generally doesn't perform one-off work for a single development team, but this should serve as a fair example of the type of overall, reusable tooling we develop.
