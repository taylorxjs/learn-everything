Git创建Develop分支的命令:

~~~bash
git checkout -b develop master
~~~

将Develop分支合并到Master分支的命令：

~~~bash
	# 先切换到Master分支
  git checkout master

  # 对Develop分支进行合并
  git merge --no-ff develop
~~~

删除Develop分支：

~~~bash
git branch -d develop
~~~

