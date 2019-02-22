#常用命令总结

1. `git init`：本地初始化代码库

2. `git clone https://github.com/XXXX/XXX`: 克隆代码库到本地

3. `git remote add origin git@github.com:xxxx/learngit.git`：在本地初始化好的仓
    库连接到指定远程仓库。

4. `git add file-name`：将本地工作目录(workfile)的改动提交到暂存(.git/index);

5. `git commit file-name -m "comment-string"`：将index中的改动提交到本地的代码库(.git)

6. `git push <远程主机名> <本地分支名>:<远程主机下分支>` 将本地分支推送到远程主机下的对应分支。
    + `git push -u orign master`：我们第一次推送master分支时，使用`-u`

    + `git push origin master`：将本地代码库master分支的改动推送到远程代码库；

    + `git push origin branch-name`:将本地branch-name分支上的改动推送到远程主机origin(github 默认远程主机位origin)的对应分支上；

    + `git push :branch-name`：删除远程主机origin下的branch-name分支，等同于`git push origin --delete branch-name`.

7. `git branch branch-name`：新建分支branch-name；

8. `git checkout branch-name`：切换到branch-name分支；

9. `git checkout -b branch-name`：新建branch-name分支，并且切换发到branch-name分支。

10. `git branch -d branch-name`：合并之后删除分支，合并之前强制删除分支使用`-D`。 

11. `git checkout --file-name`：在添加到暂存区之前撤销对工作区文件的修改；

12. `git reset HEAD file-name`：撤销暂存区的修改；

13. `git reset --hard HEAD^`:退回上一个版本，通常用字啊提交到本地仓库之后，但是还没有push时。

    + `HEAD` 表示本版本；

    + `HEAD^`：表示上一版本；

    + `HEAD^^`：表示上上版本；

    + `HEAD~100`：表示往上的第100个版本。

14. `git merge --no-ff -m "comments" branch-name`：非fast forward 合并分支，并且创建新的提交。

15. `git log --graph pretty=online`：查看提交日志。

16. `git relog`：查看提交版本的版本号。 