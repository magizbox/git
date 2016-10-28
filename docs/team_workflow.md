## Team Workflow

In this article, I will represent our workflow with git to collaboration. As you can see, there are `upstream`, `A`, `B` repositories. Upstream repostiroy is main repository of project, owner by team leader. `A` and `B` repositories belong to developers. In `upstream` remote, there are `master` and `develop` branches. In developer's repositories, there are `develop` and `feature-something` branches.

![resources/workflow.png](resources/workflow.png)

### Step 1: Create new project

In step 1, leader create a repository.

![resources/workflow-step-1.png](resources/workflow-step-1.png)

### Step 2: Forking

In step 2, each developers create their own repository by forking main repository

![resources/workflow-step-2.png](resources/workflow-step-2.png)

### Step 3: Commits

In step 3, developers work on their branches, each peace of their works should be end by a `commit`

![resources/workflow-step-3.png](resources/workflow-step-3.png)

### Step 4: Merge Requests

After finish a feature, each developer will create a `merge requests` to main repository. Leader take responsibility for merging their requests

![resources/workflow-step-4.png](resources/workflow-step-4.png)

### Step 5: Fetch and Rebase

Developer will checkout to `develop` branch, fetch from upstream remote and rebase

![resources/workflow-step-5.png](resources/workflow-step-5.png)

### Step 6: Develop new features

**Team sync**. At this moment, developer can `checkout` from `develop` branch to create new feature.

![resources/workflow-step-6.png](resources/workflow-step-6.png)

### Step 7: New version

Leader take responsibility to merge from dev branch to master branch and create tag to release new version.

![resources/workflow-step-7.png](resources/workflow-step-7.png)

## Related Readings

* ["Git With Development, Staging And Production Branches". *stackoverflow.com*. N.p., 2016. Web. 28 Oct. 2016.](http://stackoverflow.com/questions/15072243/git-with-development-staging-and-production-branches)
* ["A Successful Git Branching Model". *nvie.com*. N.p., 2016. Web. 28 Oct. 2016.](http://nvie.com/posts/a-successful-git-branching-model/)
