### Branches

A <strong>branch</strong> represents an independent line of development. Branches serve as an abstraction for the <em>edit &gt; stage &gt; commit</em> process discussed in Git Basics, the first module of this series. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

<p style="text-align:center;">git branches diagram</p>

<p style="text-align:center;"><img class="alignnone" src="http://backlogtool.com/git-guide/en/img/post/stepup/capture_stepup1_5_6.png" alt="" /></p>

<strong>Local Branches</strong>

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

<strong>Remote Branches</strong>

[^3]

```
# delete remote branches
git push origin --delete [branchname]
```

<h3>Repositories</h3>

<blockquote>
  what is <code>origin</code>?
</blockquote>

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




## Tips

[^10] [^11]

```
# Create an archive of files from a named tree
git archive --format=zip HEAD > app.zip
```

## Dev & Release with Git

![](https://lh3.googleusercontent.com/b4wC83vaEZaGkwSLV4TVlh7T8a4PEV5UnAHjFJGyNWROHGiEVR4xQtUHTPUtOZeRyERUKcfNfSHbFg=w369-h501-no)

### `Fork` & create a `Pull Request` with Github

[^12] [^13]

1. In a reposiroty you want to fork, click `Fork` button. It will create your own repository
2. Run this:

```
git remote add origin [your_repository] # that have created when you fork
git remote add upstream [original_repository] # the repository that you have fork
```

3. Code in your own repository & commit
4. Go to your Fork repository
5. Switch to your branch
6. `Create Pull Request` to send a merge request to the owner of the original repository

### Description

* **Development Branch**
  * It use for debugging, coding, testing
  * It must have `code` and `tests`
* **Release Branch**
  * It use for running, including
  * It must have `documents` (`API.md`, `HOW_TO_INSTALL.md`, `HOW_TO_RUN.md`) and `resources` (executable and resource files) in `release` folder.
  * Release Branch doesn't care about code. It only care about `release` folder.

### Rule of thumb

* Rule 1: Don't code in 2 `dev` components at the same time. Do write tests instead.
* Rule 2: Do pull `release` before switch code from a component to other.
* Rule 3: Do include `release` version of other components in case reuse (component A include component B).
* Rule 4: Don't **code** and **debug** in `release` branch, only `merge`  or `pull` (from `dev`)

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
