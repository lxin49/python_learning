# Learning Python3 with Git

## Git Usage

### 创建配置文件
1. git config --global user.name
2. git config --global user.email
3. git config --list

### 本地使用
1.  git init 初始化当前目录为工作区

2.  git add file/dir/* 添加文件/目录/*至暂存区
3.  git rm --cached 取消文件暂存记录
4.  git commit [optional]file/dir/* -m 'msg' 添加至仓库区
        .gitignore
5.  git log 查看commit日志
6.  git checkout -- file 恢复至某个commit点文件
7.  git mv/rm
8.  git reset --hard Head/commit_id
9.  git reflog 查看commit记录

10. git tag 创建tag标签
11. git show 查看标签(仅能查看当前标签?)
12. git tag -d tagname 删除标签

13. git stash save 'msg' 创建未保存工作区
14. git stash list 查看未保存工作区
15. git stash apply stash@{n} 应用工作区
16. git stash drop stash@{n} 删除工作区

17. git branch 查看现有分支
18. git checkout [branch] 创建分支
19. git checkout -b [branch] 创建分支并进行切换
20. git merge [branch] 合并分支
        两种情况:
        一是先后合并,主分支文件不变,从分支文件变化,合并时需要确认命令
        二是主从分支有相同文件进行修改,需要人工确认修改

### 连接远程服务器使用
1.  git clone xxx 获取远程项目

2.  git remote add origin xxx 连接远程项目,其中可能涉及到ssh公钥的使用
3.  git remote rm xxx 断开远程连接项目
4.  git push -u origin master/[branch] -> git push 上传至远程网络
        git push --force origin 强制推送
5.  git pull origin master/[branch] 从远程网络获取
