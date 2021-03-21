Git is a distributed version control system.
Git is free software.

常用命令：
1.掌握工作区的状态(是否有文件被修改
	git status
2.把文件添加到仓库
	git add 1.txt 2.txt
3.把文件提交到仓库
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


