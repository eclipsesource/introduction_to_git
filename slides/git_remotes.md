.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
 ### - Branches
 ### - Merging
 ### - Remotes
]

.right-column[
90% of all activity you perform will be on your **own** Git Repository. However,
to be able to collaborate, you need to manage your **remote repositories**.

GitHub is an example of a **remote repository**, but it's just one example.
Remote repositories are versions of your project that are hosted on the
Internet or network somewhere. You can have multiple remote repositories.

Use `git remote -v` to list your remotes.

<img src="images/git-remotes.png" class="centered" width="500px"/>

Use `git remote add <shortname> <url>` to add a new remote.

If you `clone` a repository, Git will automatically add a remote named
`origin` for you.

]
---
.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
 ### - Branches
 ### - Merging
 ### - Remotes
]

.right-column[
###Fetching and Pulling from Remotes
`git fetch [remote-name]` will pull down all the data from that remote.

`git pull [remote-name]` will automatically fetch and merge for you. This
requires your current branch to be configured to track a remote branch.

.listWithHeader[When you are ready to push data, use  
`git push [remote-name] [branch-name]`.
* You must have **write access** to the remote repository
* You must be **up to date**
]

If you are not **up to date** you will need to fetch their work and incorporate
it into yours before you can push.
]
