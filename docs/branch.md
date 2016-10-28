# Branches

A <strong>branch</strong> represents an independent line of development. Branches serve as an abstraction for the <em>edit &gt; stage &gt; commit</em> process discussed in Git Basics, the first module of this series. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

<center>*git branches diagram*</center>

<p style="text-align:center;"><img class="alignnone" src="http://backlogtool.com/git-guide/en/img/post/stepup/capture_stepup1_5_6.png" alt="" /></p>

**Local Branches**

```
# view branches
git branch
# create new branch
git checkout -b [branchname]
# switch to a branch
git checkout [branchname]
# delete branch
git branch -D [branchname]
```

<strong>Merge Branches</strong>

```
git merge [branchname]
```

<strong>Remote Branches</strong>[^3]

```
# delete remote branches
git push origin --delete [branchname]
```

## Repositories

>  what is <code>origin</code>?

```
# view remote branches
git remote -v
# add remote branches
git remote add [repositoryname] [branch_url]
# clone a repository into a new directory
git clone
# push to repository
git push [repositoryname] [branchname]
git pull
```
## Branch Naming Convention


* Choose *short* and *descriptive* names:

```
# good
$ git checkout -b oauth-migration

# bad - too vague
$ git checkout -b login_fix
```

* Identifiers from corresponding tickets in an external service (eg. a GitHub issue) are also good candidates for use in branch names. For example:

```
# GitHub issue #15
$ git checkout -b issue-15
```

* Use *dashes* to separate words.

* When several people are working on the same feature, it might be convenient to have personal feature branches and a team-wide feature branch. Use the following naming convention:

```
$ git checkout -b feature-a/master # team-wide branch
$ git checkout -b feature-a/maria  # Maria's personal branch
$ git checkout -b feature-a/nick   # Nick's personal branch
Merge at will the personal branches to the team-wide branch (see "Merging"). Eventually, the team-wide branch will be merged to "master".
```

* Delete your branch from the upstream repository after it's merged, unless there is a specific reason not to.

* Tip: Use the following command while being on "master", to list merged branches:

```
$ git branch --merged | grep -v "\*"
```


## Create an archive

[^10] [^11]

```
# Create an archive of files from a named tree
git archive --format=zip HEAD > app.zip
```

## Fork & Request

[^12] [^13]

1. In a repository you want to fork, click `Fork` button. It will create your own repository
2. Run this:

```
git remote add origin [your_repository] # that have created when you fork
git remote add upstream [original_repository] # the repository that you have fork
```

3. Code in your own repository & commit
4. Go to your Fork repository
5. Switch to your branch
6. `Create Pull Request` to send a merge request to the owner of the original repository


[^2]: <a href="https://www.atlassian.com/git/tutorials/using-branches/" target="_blank">https://www.atlassian.com/git/tutorials/using-branches/</a>
[^3]: <a href="http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely/2003515#2003515" target="_blank">http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely/2003515#2003515</a>
[^4]: <a href="https://guides.github.com/features/issues/">https://guides.github.com/features/issues/</a>
[^5]: <a href="https://help.github.com/articles/using-pull-requests/" target="_blank">https://help.github.com/articles/using-pull-requests/</a>
[^6]: <a href="https://help.github.com/articles/about-github-wikis/" target="_blank">https://help.github.com/articles/about-github-wikis/</a>
[^7]: <a href="https://help.github.com/articles/about-repository-graphs/" target="_blank">https://help.github.com/articles/about-repository-graphs/</a>
[^8]: <a href="https://help.github.com/articles/closing-issues-via-commit-messages/" target="_blank">Closing an issue in the same repository</a>
[^9]: [Git Tools - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
[^10]: [Git: how to get all the files changed and new files in a folder or zip?](http://stackoverflow.com/questions/4126300/git-how-to-get-all-the-files-changed-and-new-files-in-a-folder-or-zip)
[^11]: [git-scm.com: git-archive](https://git-scm.com/docs/git-archive)
[^12]: [Forking a Repo](https://help.github.com/articles/fork-a-repo/)
[^13]: [Using pull request](https://help.github.com/articles/using-pull-requests/)
