###设置用户名和邮箱
```
git config --global user.name "ShirleyTse"
git config --global user.email "ssshirleytse@hotmail.com"
```
###别名Alias的设置
```
git config --global alias.co checkout //把checkout设置为co
git config --global alias.ci commit //把commit设置为ci
```
###diff
```
git diff  //查看做了哪些改动
          //只能比较当前文件和暂存区文件差异
```
###checkout
#####到切换分支、tag、comiit
```
git checkout branch
git checkout v1.0
git checkout ...  //...是commit_id，是每次commit的SHA1值，可以根据git log。
```
#####撤销还没add进暂存区的文件
`git checkout a.md`
###stash
```
git stash  //把当前分支所有没有commit的代码暂存起来
git stash list  //查看暂存区
git stash apply //还原代码
git stash drop  //删除stash记录
git stash pop   //apply+drop
```
###merge & rebase
```
git checkout master
git merge featureA   //把分支featureA合并到主分支master上
```
```
git checkout master
git rebase featureA  //rebase也是合并
```