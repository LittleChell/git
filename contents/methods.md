## git 常见事例指南：

### 回退操作

---

#####
**Undoing a git 使用git reflog查看commit ID执行回退操作**<br>
[1-_reflog_-_stackoverflow_](https://stackoverflow.com/questions/134882/undoing-a-git-rebase)<br>
[2-_reflog_-_stackoverflow_](https://stackoverflow.com/questions/2510276/undoing-git-reset)

**Revert Git repository to a previous commit git会退到先前的commit**<br>
[ _revert_-_reset_-_stackoverflow_](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit)

通过使用git revert回撤某个或多个commit，会把这些commit涉及到的文件修改撤销掉，同时会变成modify等的状态，通过提示可以使用git reset/git add的方式使用/丢弃该文件的commit。
both modify的可以通过git checkout --theirs path/git checkout --ours path选择性地来使用/丢弃之前的commit。
这样就可以选择性地选用或者丢弃某些commit里面的一些文件修改。

**撤销unstaged的文件-git checkout**<br> 	
	git checkout --.可以撤销当前路径下面所有已改动但未放到暂存区的文件。<br>
	git checkout filename1 filename2 ... 可以撤销未放到暂存区的文件<br>

**撤销staged的文件-git reset**<br>
git reset	可以撤销已加入到暂存区的所有文件使之回到未加入暂存区时候的状态<br>
git reset filename1 filename2 ... 可以撤销已加入到暂存区的文件使之回到未加入暂存区时候的状态

**回退某个文件到指定的commit-git checkout**<br>
git checkout <commit hash\> --(可选，效果不变) path/file1  path/file2 ...
注意：这里checkout是使文件回到其放到暂存区的状态<br>回到之前的一个版本只需要在<commit hash\>后加上~1<br>
git reset <commit hash\> <filename\>
这里是直接回退文件到那个版本，可以加上--hard

---
