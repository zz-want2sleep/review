*   创本地仓库前还是把远程仓库在github里面==先创好==。

*   git init

*   git pull  `拉取从远程仓库获取的资源`

*   然后git add .

*   git commit -m '注释'

*   `git remote add origin https://github.com/xxxx/xxx.git或者是ssh形式的url`用来创建远程版本库origin，并完成对接。

*   `git push -u origin master`本地传递数据到远程库==-u==为第一下上传需要以后直接`git push`。

    其余的以后写

    ---
    
    **错误**：==There is no tracking information for the current branch.
    Please specify which branch you want to merge with.
    See git-pull(1) for details.==
    
        git pull <remote> <branch>
    
    If you wish to set tracking information for this branch you can do so with:
    
        git branch --set-upstream-to=origin/<branch> master

**解决方法**：是因为本地分支和远程分支没有建立联系  (使用git branch -v 可以查看本地分支和远程分支的关联关系)  .根据命令行提示只需要执行以下命令即可

 

**git branch --set-upstream-to=origin/远程分支的名字 本地分支的名字**

==还不行就按下面来==。

*   a、首先检查本地库有没有已经关联的远程库，如果已经有了可以删除，或者可以重新建立一个，别重名

**查询： git remote -v**

*   查询之后，发现已经关联了两个远程库，可以先删除这种关联。
    删除：git remote remove origin

    000@WIN-5B0M5RN6I1I MINGW64 /e/Git_Repository (master)
    $ git remote remove origin

    000@WIN-5B0M5RN6I1I MINGW64 /e/Git_Repository (master)
    $ git remote -v

*   新建：git remote add origin 远程库的地址（可以使用https或者ssh的方式新建）

    000@WIN-5B0M5RN6I1I MINGW64 /e/Git_Repository (master)
    $ git remote add origin  git@github.com:wet5649/tedu.git


*   然后git add .
*   git commit -m '注释'
*   `git push -u origin master`本地传递数据到远程库==-u==为第一下上传需要以后直接`git push`。