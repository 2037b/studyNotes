# git 和 github 区别，基础知识

Git 能记录每次文件的改动，git 是 分布式版本控制系统，没有中央服务器，每个人的电脑就是一个完整的版本库。

**区别于**  集中式版本控制系统 ：所有文件均存于服务器，服务器无法启动则数据无法更新、回滚。

git是 工具 无需联网；github是 托管平台，保存 每一次 不同用户 所提交的修改记录。  

用户 之间互相推送的是 修改记录 而不是整个 仓库。

## git 学习

配置 用户名 和 邮箱号  
$ git config --global user.name "Your Name"  
$ git config --global user.email "email@example.com"  


创建版本库 .git ，将 当前目录 变为git可管理的仓库  
$ git init  


将 文件 添加到 暂存区(stage)  
$ git add <文件名.后缀>  

将 暂存区的所有内容 提交到 当前分支 默认 master分支(一次提交多个文件)  
$ git commit -m "<本次提交说明>"  

查看当前 版本库 的状态
$ git status  
比较 分支上的文件 与 工作区的文件  
$ git diff <文件名.后缀>  
查看 分支 的 提交日志
$ git log  
特定格式输出  
$ git log --pretty=oneline  
HEAD 类似 指针 ，存在于 分支中 指向当前 版本号，通过调整 HEAD 实现版本 更新 或者 回退  
$ git reset --hard HEAD^  
查看所有分支的所有操作记录。
$ git reflog  
回退版本  
$ git reset --hard <指定版本>  
$ git diff HEAD -- <文件名.后缀>   
将 本地仓库 与 远程仓库 关联
$ git remote add origin git@github.com:michaelliao/learngit.git  