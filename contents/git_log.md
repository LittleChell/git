# git log 指令

## 参考资料：
* [git log官方API](https://git-scm.com/docs/git-log)

## 实践总结：
* 该指令一般用来回退（配合git reset），或查找历史记录（配合git diff）；

## git log 常用指令：
* git log
	* 查看commit提交历史, 查看commit id方便回退；

* git log -p filename
	* 查看文件的每一个详细的历史修改，如果没有-p选项，只显示提交记录，不显示文件内容修改，git log -p -3 filename 显示最近的3次提交。

* git log --pretty=oneline (filename)
	* 简短形式显示 commit 提交历史；(只显示每一次commit的id以及注释)
	* 加上filename就是显示某个文件的修改历史；

* git log --oneline --graph --decorate
	* 简短形式显示当前分支提交记录以及源分支信息（查看当前分支是基于哪个分支创建）；

* git log --left-right branchA...branchB
	* 返回两个分支间的commit差异；

* git reflog
	* 查看本地仓库所有改变列表（git reset的每次操作都会记录在该列表）

## Tips：
* 查看某次commit的修改内容使用

	git show < commit ID >

## 相关指令：
* [git reset](https://github.com/LittleChell/git/tree/master/contents/git_reset.md) 代码撤销（回退）指令： `git log`好基友！
