#### Git合并不同url的项目
- 使用命令git remote add [shortname] [url]将老Git url加到我们新Git的本地
- 这里我把他取名为base-dev（随便取）
- 使用命令git remote -v查看远程仓库的情况
- 使用命令git fetch base-dev刷新远程仓库到本地
- 使用命令git merge base-dev/master合并项目
- base-dev是指代仓库，master指代分支，当然如果有需要也可以合并别的分支过来 
- 再提交就成功了

