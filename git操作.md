#### 基本操作

pwd	查看当前目录

git init 初始化仓库

git add filename  将文件添加到暂存区

git commit -m 注释   将暂存区的文件提交到仓库，-m后面为此次提交注释

git status 查看当前状态

git diff filename	查看文本文件变化的内容

#### 版本回退

git log	查看版本提交日志

git log-pretty=oneline	以行形式查看日志

git reset --hard HEAD^	回退到上一个版本

git reset --hard Head ~n	回退到上n个版本

git reflog 	查看以往所有版本版本号（包括回退的）

git reset --hard 版本号	回退到版本号对应的版本

#### 撤销修改和删除文件

git chechout ==--== filename 撤销还未添加在暂缓区中的在工作区做的修改

rm filename	删除工作区中的文件（也可以直接右键删除）

要想在库中也删除，需在工作区删除后git commit提交

撤销同理，git checkout -- filename

#### 远程仓库

git remote add origin github仓库链接	将本地仓库与github上的远程仓库链接起来

git push	将本地仓库内容推送到远程仓库

git clone 仓库链接 	克隆远程仓库到本地目录

#### 创建与合并分支

git check -b branchname	  创建并切换分支

相当于git branch branchname  和    git checkout branchname

git branch	列出所有分支，*指向当前分支

git merge branchname	在master分支上使用，使其他分支合并到master

git branch -d branchname	删除分支

#### 工作保存

保存当前分支工作，先去做其他分支工作

git stash

git stash list	查看保存的工作区列表

git stash apply	恢复保存的工作区不删除

git stash drop	删除一条保存的工作区

git pop 	恢复并删除

#### 多人协作

当你从远程库克隆时候，实际上Git自动把本地的master分支和远程的master分支对应起来了，并且远程库的默认名称是origin。