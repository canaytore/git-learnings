# Git - Version Control System

Using Git as a source code management tool has become an essential skill for all web developers. Git helps us to manage the code in a project as we develop new features, helps to find and fix problems, and simplifies collaboration with other developers around the world. Git has helped me manage complex projects, and I firmly believe, helps me to write better code too.

Git is software that keeps track of changes that we make to files and directories. And it's especially good at keeping track of text changes. It allows you to move back and forth between the versions. And to compare the different versions to see what changed. Git is referred to as a *Version Control System (VSC)*. Git's not the first version control system ever created, there've been others. And almost all of them had one primary purpose, to manage source code. Programmers wanted a way to be able to track the changes that they made to computer code over time, as they added features and as they fixed bugs. So they created version control. Because of this they're also called *Source Code Management (SCM)* tools. The two terms are used pretty interchangeably.

Git is **distributed version control**. Different users each maintain their own repositories instead of working from a central repository, and the changes are stored as *sets* or *patches*, and we're focused on tracking changes, not the versions of the documents. That's a subtle difference; CVS and SVN, those track changes too. They track the changes that it takes to get from version to version of each different file, or the different states of a directory. Git doesn't work that way. Git really focuses on these change sets, and encapsulating a change set as a discrete unit, and then those change sets can be exchanged between repositories. Git is not trying to keep up to date with the latest version of something. Instead the question is do we have a change *set* applied or not? So you might say that you merge in change *sets* or you apply *patches* between the different repositories. So there's no single master repository. There's just many working copies, each with their own combination of change sets. 

Because it's distributed, that has a couple of advantages. It means that there's no need to communicate with a central server, and that makes things faster and it means that it's not necessary to have network access to submit our changes. With CVS and SVN, if something goes wrong with that central repository, that can be a real show stopper for everyone else who's working off of that central repository. With Git, everyone can keep working. They've each got their own repository that they're working from, not just a copy that they're trying to keep in sync with some central repository. It also encourages participation in *forking* projects, and this is really important for the open source community because developers can work independently. They can make changes, they can make bug fixes, feature improvements, and then they can submit those back to the project for either inclusion or rejection. Even if we're working on an open source project and we don't like the way that it's going, we can fork that project, create our own version and take it in a completely different direction. That becomes a really powerful and flexible feature that's well suited to collaboration between teams, especially loose groups of distributed developers.

**Table of contents:**
- [01 - Basic Git Configurations.md](01-git%20config.md)
- [02 - Git help](02-git%20help.md)
- [03 - Initialize a repository](03-git%20init.md)
- [04 - Git's Three-Tree Architecture](04-three-tree%20architecture.md)
- [05 - Git commit](05-git%20commit.md)
- [06 - Git log](06-git%20log.md)
- [07 - View Changes with Git diff](07-git%20diff.md)
- [08 - Delete Files](08-git%20rm.md)
- [09 - Move and Rename Files](09-git%20mv.md)
- [10 - Git checkout](10-git%20checkout.md) [WIP]
- [11 - Revert a commit](11-git%20revert.md) [WIP]

**Author:**
- Can Ayt??re - [github/canaytore](https://github.com/canaytore)
