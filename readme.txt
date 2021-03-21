Git is a distributed version control system.
Git is free software.

常用命令：
1.掌握工作区的状态(是否有文件被修改
	git status
2.把文件添加到仓库 (把文件修改添加到暂存区)
	git add 1.txt 2.txt
3.把文件提交到仓库 (把暂存区的所有内容提交到当前分支)
	git commit -m "说明"
4.查看未提交版本与提交版本的区别
	git diff file.txt
5.查看从最近到最远的提交日志
	git log --pretty=oneline
6.回退到上一个版本 (HEAD表示当前版本，HEAD^表示上一个版本，HEAD^^表示上上个版本,HEAD~100表示往上100个版本)
	git reset --hard HEAD^
7.回到某个指定到版本(指定版本号，版本号可以不写全，回退到上上个版本后，若还记得上个版本到版本号，还能再退回去（用git reflog 查看）
	git reset --hard d862fa
8.得到你的每一次提交回退命令
	git reflog
9.撤销工作区的全部修改(未添加到暂存区)，回到上一次add或者commit之后的状态，
--一定要，checkout不带--则表示切换分支
	git checkout -- file.txt
10.撤销暂存区的修改,HEAD表示最新到版本(已经提交到分支)
	git reset HEAD file.txt
11.删除文件,未提交的文件直接从工作区删除，已经提交的用命令删除,然后重新commit
	git rm file.txt
12.恢复在本地被删除的文件到已经提交的最新版本（若提交到版本库的已经删除，就没办法啦）
	git checkout -- file.txt
远程仓库
1.关联远程仓库，添加前需要将本地rsa密钥到远程仓库的账户列表中(origin)即远程库的名字
	git remote add origin git@github.com:zffsgit/git.git
2.推送本地库的所有内容推送到远程分支（-u将本地分支与远程分支进行关联，第一次推送分支时使用）
	git push -u origin  master
3.查看远程库的信息
	git remote -v
4.删除远程库(解除了本地和远程的绑定关系,没有真到删除远程库）
	git remote rm origin
5.克隆远程仓库
	git clone git@github.com:zffsgit/c++.git
6.创建分支
	git branch nb
7.切换到已有分支
	git checkout nb / git switch nb
8.创建并切换分支
	git checkout -b nb / git switch -c nb
9.查看当前分支
	git branch
9.查看包括远程分支在内到工作目录下的所有分支
	git branch
10.合并指定分支(eg.nb)到当前分支(eg.master)
	git merge nb
11.删除分支
	git branch -d nb
12.

