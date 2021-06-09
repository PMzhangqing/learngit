### 常用命令

- git init（创建版本库）
- git add "fileName"（将修改文件加入提交列表）
- git commit -m "注释"（提交）
- git log（查看版本）
- git log --pretty=oneline（查看版本，单行显示）
- git reset --hard HEAD^  （返回上一个版本）
- git reset --hard 1094a（返回到某版本，版本号没必要写全，前几位就可以了，Git会自动去找）
- git reflog（用来查询你的每一次命令）
- get status （查看状态）
- git diff HEAD --fileName（查看工作区和版本库里面最新版本的区别）
- git checkout -- fileName（丢弃工作区的修改）
- git reset HEAD fileName（把暂存区的修改撤销掉，重新放回工作区）
- get rm "fileName"（删除文件）

- `HEAD`指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令`git reset --hard commit_id`。
- 穿梭前，用`git log`可以查看提交历史，以便确定要回退到哪个版本。
- 要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。



### 远程仓库

- 要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；
- 关联一个远程库时必须给远程库指定一个名字，`origin`是默认习惯命名；
- 关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；
- 此后，每次本地提交后，只要有必要，就可以使用命令`git push origin master`推送最新修改；
- 如果添加的时候地址写错了，或者就是想删除远程库，可以用`git remote rm <name>`命令。使用前，建议先用`git remote -v`查看远程库信息：
- `git clone git@github.com:server-name/repo-name.git`克隆一个本地库



### 分支管理

