# git push 指令

## 参考资料：
* [git push 官方API](https://git-scm.com/docs/git-push)
* [git push 日常指令-Git教程](http://www.yiibai.com/git/git_push.html)
* [git push 默认行为](https://segmentfault.com/a/1190000002783245)

## 实践总结：
* git push <远程主机名> <本地分支名>:<远程分支名>
* 如果当前分支与远程分支之间存在追踪关系，则本地分支和远程分支都可以省略。
* `git push origin`
* 上面命令表示，将当前分支推送到origin主机的对应分支。

## git push 常用指令：
* git push
	* 推送代码至与当前分支关联的远程分支
* git push -f
	* 将当前分支的commit强制推送到远程分支（不处理 更新、合并等， 非常危险的指令，谨慎操作）

* git push origin remoteBranchName
	* 推送代码至指定的远程分支

* git push origin newBranch:newBranch
	* git push <远程主机名> <本地分支名>:<远程分支名>
	* 推送分支到远程并在远程创建一同名分支， ’newBranch’为本地分支名，远程不存在同名分支

* git push origin --delete [branch-name]
  * 删除远程分支

## git push 默认行为

git的全局配置中，有一个push.default属性，其决定了git push操作的默认行为。在Git 2.0之前，这个属性的默认被设为'matching'，2.0之后则被更改为了'simple'。

我们可以通过git version确定当前的git版本（如果小于2.0，更新是个更好的选择），通过git config --global push.default 'option'改变push.default的默认行为（或者也可直接编辑~/.gitconfig文件）。

push.default 有以下几个可选值：
nothing, current, upstream, simple, matching

其用途分别为：

nothing - push操作无效，除非显式指定远程分支，例如git push origin develop（我觉得。。。可以给那些不愿学git的同事配上此项）。

current - push当前分支到远程同名分支，如果远程同名分支不存在则自动创建同名分支。

upstream - push当前分支到它的upstream分支上（这一项其实用于经常从本地分支push/pull到同一远程仓库的情景，这种模式叫做central workflow）。

simple - simple和upstream是相似的，只有一点不同，simple必须保证本地分支和它的远程
upstream分支同名，否则会拒绝push操作。

matching - push所有本地和远程两端都存在的同名分支。

## 相关指令：
* [git_status.md](https://github.com/LittleChell/git/tree/master/contents/git_status.md)  查看当前代码状态指令： 使用我这个指令，只是为了确认提交远程是否成功而已。。。
