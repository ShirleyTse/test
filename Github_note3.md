###Git Branch Management
```
git branch develop  //create a branch named deverlop
```
Explanation: The command to create a new branch is based on all the current branches. So if now you are in branch master, and you create "develop" based on it. It turns out that the content of develop is as same as master.

```
git checkout develop  //switch to develop
git checkout -b develop  //create develop and switch to it automatically
git push origin develop   //push develop to remote repositories
git branch  //look up local branch list
git branch -r  //look up remote branch list
git branch -d develop   //delete 
git branch -D develop   //delete forcibly
git push origin :develop  //delete remote branch
git checkout develop origin/develop  
//if the remote branch has a develop, while the local has not, you want to  move the remote develop to the local.
git checkout -b develop origin/develop  //move develop from local to remote
```
####Git FLow
![](http://m.qpic.cn/psb?/V12MRciw2Hiprn/ja03FAO*jiOnDRHYw3NsMSrjdLpG*nGxU57KUacEQLA!/b/dLkAAAAAAAAA&bo=LAR8BQAAAAARB2E!&rf=viewer_4)
Generally, there are two branches which are master and develop. Their duties are:

master: in production-ready state all the time

develop: latest developing state

On the other hand, there are Auxiliary branches to help emergency repair.

feature: develop new functions, based on develop, merge to develop after completed

release: repair bugs, based on develop, merge to develop & master after completed

hotfix: fix problems of master, based on master, merge to master & develop after completed


Let's suppose that we've already have master and develop. And we are going to create a function named A. So the first step is to create a branch based on develop.

`git branch feature/a`

Here is a standard: all of the function branches should use 
"feature" as prefix.

At this time, we notice that there is a urgent bug that needs to fix. So we switch to the master, and create a new branch based on it.

`git branch hotfix/B`

After repairing work, we create a release branch.

`git branch release/1.0`

We do final tests on this branch. If we find any bug, we modify them straightly, until the tests are ok.


