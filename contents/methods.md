## git 常见事例指南：

### 回退操作

#####
[Undoing a git 使用git reflog查看commit ID执行回退操作1 _reflog_-_stackoverflow_](https://stackoverflow.com/questions/134882/undoing-a-git-rebase)

[Undoing a git 使用git reflog查看commit ID执行回退操作2 _reflog_-_stackoverflow_](https://stackoverflow.com/questions/2510276/undoing-git-reset)

[Revert Git repository to a previous commit git会退到先前的commit _revert_-_reset_-_stackoverflow_](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit)
	
git checkout --.可以撤销当前路径下面所有已改动但未放到暂存区的文件。<br>
git checkout filename1 filename2 ... 可以撤销未放到暂存区的文件<br>

git reset	可以撤销已加入到暂存区的所有文件使之回到未加入暂存区时候的状态<br>
git reset filename1 filename2 ... 可以撤销已加入到暂存区的文件使之回到未加入暂存区时候的状态