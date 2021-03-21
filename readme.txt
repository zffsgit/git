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
11.删除文件

