### Git提交代码的流程
- **git stash** （这是将本地代码回滚值至上一次提交的时候，就是没有你新改的代码）
- **git pull origin** 远程分支名（将远程的拉下来）
- **git stash pop**（将第一步回滚的代码释放出来，相等于将你修改的代码与下拉的代码合并）
- 然后解决冲突，你本地的代码将会是最新的代码
- **git add .**（后面有一个点，意思是将你本地所有修改了的文件添加到暂存区）
- **git commit -m""**(引号里面是你的介绍，就是你的这次的提交是什么内容，便于你以后查看，这个是将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中)
- **git pull origin** （没有123步时使用） 远程分支名 这是下拉代码，将远程最新的代码先跟你本地的代码合并一下，如果确定远程没有更新，可以不用这个，最好是每次都执行以下，完成之后打开代码查看有没有冲突，并解决，如果有冲突解决完成以后再次执行4跟5的操作
- **git push origin master**（git push origin 本地分支名:refs/remotes/远程分支名） 将代码推至远程就可以了
### Git合并不同url的项目
- 使用命令**git remote add [shortname] [url]**将老Git url加到我们新Git的本地
- 这里我把他取名为**base-dev**（随便取）
- 使用命令**git remote -v**查看远程仓库的情况
- 使用命令**git fetch base-dev**刷新远程仓库到本地
- 使用命令**git merge base-dev/master**合并项目
- base-dev是指代仓库，master指代分支，当然如果有需要也可以合并别的分支过来 
- 再提交就成功了

### Git回退代码到指定版本
- 查看所有的历史版本，获取你git的某个历史版本的id， **git log**
- 回退本地代码库：**git reset --hard ID**
- 推送到远程服务器：**git push -f -u origin master**
- 重新拉代码：**git pull**