## git 常见问题：

1.	#####秘钥设置

	.ssh生成的公钥全部复制然后粘贴到gitHub上，公钥是放在.ssh文件夹里面的，复制前先找到这个文件夹


2.	#####基于远程分支创建本地分支

	git checkout -b <localbranch> origin/<remotebranch>

3.	#####删除远程分支

	git push origin :<branch-name>

4.	#####查找回退的commit ID

	使用git log或者git reflog找到回退的ID。



