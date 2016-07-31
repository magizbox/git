### Branches

[^2]

<blockquote>&lt;check in�early, check in often&gt; what is `master`?</blockquote>

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

<strong>Merge�Branches</strong>

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

### Git Configurations

Known Issues

* [How do I force git to use LF instead of CR+LF under windows?](http://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-windows)

```
git config --global core.autocrlf false
```

<h3>Power Tools with Github</h3>

<img class="alignnone" src="https://lh3.googleusercontent.com/jxrgdB4uS2wUn_C2X1W1n5wNtBVi4Yu4BokdjoKJmpMO=w42-h39-no" alt="" /> <strong>Issues &amp; Milestones</strong> [^4]
<blockquote>Issues are a great way to keep track of tasks, enhancements, and bugs for your projects. They�re kind of like email�except they can be shared and discussed with the rest of your team. Most software projects have a bug tracker of some kind. GitHub�s tracker is called <strong>Issues</strong>, and has its own section in every repository.</blockquote>

<img class="alignnone" src="https://lh3.googleusercontent.com/bBxznG1WyiN5B7T8n4ytZUFQ7zWuFPPPF8rqHviyvDGl=w1017-h898-no" alt="" />

<strong>Code</strong>

[^8]

```
# commit to fix issue
git commit -m "fix #34"
```

<blockquote>Once you�ve collected a lot of issues, you may find it hard to find the ones you care about. <strong>Milestones</strong>, labels, and assignees are great features to filter and categorize issues. A <strong>milestone</strong> acts like a container for issues. This is useful for associating issues with specific features or project phases</blockquote>

<a href="https://github.com/scikit-learn/scikit-learn/milestones" target="_blank"><img class="alignnone" src="https://lh3.googleusercontent.com/sx5ZWGPoEIjQ2aCBIU-NOwWQq8KxFcVq0YOM6s9Hfq0z=w1003-h477-no" alt="" width="1003" height="477" /></a> <img class="alignnone" src="https://lh3.googleusercontent.com/i22KAkqUFmKYVryN0PVF5Dc-VkiA2nzYB6TenVi4GV79=w41-h39-no" alt="" />�[^5] </strong>

<blockquote><strong>Pull requests</strong> let you tell others about changes you've pushed to a repository on GitHub. Once a pull request is sent, interested parties can review the set of changes, discuss potential modifications, and even push follow-up commits if necessary.</blockquote>

<a href="https://github.com/scikit-learn/scikit-learn/pulls" target="_blank"><img class="alignnone" src="https://lh3.googleusercontent.com/Gn9AvcPAjBYdis5SMw7aka8gicw319YAhZcCZ_oswp17=w389-h320-no" alt="" /></a>

<img class="alignnone" src="https://lh3.googleusercontent.com/O1h3xeXbV7tLQ3SWTgAS4LFJqEk-N52eN66bF_eZ2ceA=w40-h37-no" alt="" width="40" height="37" />�<strong>Wiki [^6] </strong>

<blockquote>
<div class="intro">Just as writing good code and great tests are important, excellent documentation helps others use and extend your project.</div>
Every GitHub repository comes equipped with a section for hosting documentation, called a <strong><em>wiki</em></strong>.</blockquote>

<a href="https://github.com/scikit-learn/scikit-learn/wiki" target="_blank"> <img class="alignnone" src="https://lh3.googleusercontent.com/bf_-VugPSCmBAf-BHf7xXZ4-dWZ86RK5vusvjkdtmIvu=w391-h320-no" alt="" width="391" height="320" /></a>

<strong><img class="alignnone" src="https://lh3.googleusercontent.com/1HOQm2TEJl0LmJQdFVYkVQ9P6cK_j7JYfP89AjZfBTIz=w41-h38-no" alt="" /> Repository Graphs [^7]</sup></strong>

<blockquote>Every repository has <strong>graphs</strong> that display data about traffic, contributors, and commits.</blockquote>

<a href="https://github.com/scikit-learn/scikit-learn/graphs/contributors" target="_blank"><img class="alignnone" src="https://lh3.googleusercontent.com/qv_jzfMOA6RTgjrYxK6dS7Di9pA9mh2OpKVEV3gSnsOC=w1003-h742-no" alt="" width="1003" height="742" /></a>

<strong>Interview</strong>

<ul>
<li><a href="http://www.linux.com/news/featured-blogs/185-jennifer-cloer/821541-10-years-of-git-an-interview-with-git-creator-linus-torvalds">10 Years of Git: An Interview with Git Creator Linus Torvalds</a></li>
</ul>

<h2>Learn Git</h2>

<ul>
<li><a href="http://git-scm.com/docs/gittutorial">Official Git Tutorial</a></li>
<li><a href="https://backlogtool.com/git-guide/en/">Git Beginner's Guide for Dummies</a></li>
</ul>

## Git Submodule

[^9]

Add new submodule

```bash
git submodule add https://github.com/chaconinc/DbConnector
```

Update submodule

```bash
git submodule init
git submodule update
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
