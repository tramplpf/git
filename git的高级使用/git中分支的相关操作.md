#Git 通过命令行进行分支管理：
* 创建分支

        $ git branch <分支名>
* 切换分支

        $  git checkout <分支名>
* 看当前项目中，自己创建的分支

        $git  branch
* 不同分支之间的切换

    git checkout 分支名

* 切换到newBranch的远程分支

方法一   
使用git checkout -b
    
         
    git checkout -b newBranch  origin/newBranch
      
方法二    
使用git branch <branchname> [<start-point>]


    git branch newBranch origin/newBranch
    
    