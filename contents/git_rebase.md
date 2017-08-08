# git rebase 指令

## 参考资料
* [git rebase官方API](https://git-scm.com/docs/git-rebase)

## 实践总结：
* Reapply commits on top of another base tip（在某个commit基础上改变commit）


## git rebase 常用指令：
* git rebase master
	* 将当前分支 与 **本地** 叫`master`分支的代码合并, 当前分支与`master`处在同一线上，当前分支的改动将在`master`分支的下一节点上；

* git rebase --abort
	* 如果当前分支 跟 待合并的分支有冲突， 可以使用该指令取消`git rebase branchName`指令；（不想取消且你有足够耐心：可使用`git rebase --continue`和`git rebase --skip`手动一步一步完成代码合并，当然没`git merge branchName`来的有效率）

* git rebase master newBranch
	* 将`newBranch`分支代码变基到`master`分支；相当于`git checkout newBranch` + `git rebase master`;

* git rebase -i
	* 编辑本地未`push`的`commit`（本人多用于合并commit）, 注意： 该指令需要 当前分支有 关联的 远程分支；
	* 将要合并的commit前面“pick”改成（vim模式输入“i”进入编辑状态）“s”就能将它合并到前一个`commit`去, 然后保存退出(esc退出编辑状态，然后”:"输入“wq”保存退出)。
	* 退出后进入下一个编辑窗口， 主要修改合并后新的注释， 同理 输入“i”进入编辑状态， 修改完esc退出编辑状态，然后”:"输入“wq”保存退出；

## 相关指令：
* [git_merge.md](https://github.com/LittleChell/git/tree/master/contents/git_merge.md) 合并其他分支代码： 我使用的频率更高一些哦！
