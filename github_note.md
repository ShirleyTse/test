```
mkdir test  （创建文件夹）
cd test     （切换到文件夹）
touch a.md  （创建a.md）
```
```
git status  （查看git状态）
git init    （git初始化）
```
```
git add     （提交文件到仓库）
//提示Changes to be committed:表示文件等待被提交
```
```
git commit -m 'first commit'  （表示提交文件，附带信息为first commit）
```
```
git log    （查看所有提交）
```
```
git add & git commit
前者是将添加提交到一个暂缓区，临时保存改动，后者是真正的提交。
```
```
执行git init以后会默认生成一个主分支master
git branch        （查看当前分支情况）
git branch a      （创建分支a）
git checkout a    （切换到分支a）
git checkout -b a （创建并切换到分支a）
git merge         （合并到主分支master上来）
git branch -d a   （删除分支a）
git branch -D a   （强制删除分支a）
```
```
git tag v1.0      (创建标签v1.0）
git tag          （查看标签）
git checkout v1.0（切换到1.0）
```
###向github提交代码
```
ssh
ssh-keygen -t rsa （再连按三下空格，生成rsa密钥，id-rsa是密钥，id-rsa.pub是公钥）
cd ~/.ssh
cat id_rsa.pub    （查看公钥）
ssh -T git@github.comssh -T git@github.com
```
####push&pull
######push是把本地代码推到远程仓库，pull是把远程仓库的最新代码拉下来，保持两段代码的同步。
######一般先pull再push，这样不容易冲突。
```
git push origin master
git pull origin master
```
```
git clone https://github.com/ShirleyTse/test.git（克隆test项目到本地）
git remote add origin https://github.com/ShirleyTse/test.git (连接远程仓库）
```