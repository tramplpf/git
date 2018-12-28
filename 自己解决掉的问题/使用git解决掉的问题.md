# 使用git 解决掉的问题
* 安装好git之后，在正常的命令行下面执行git log 命令也为出现中文乱码现象。

    
    通过设置环境变量 LANG 的取值为 zh_CN.UTF-8 可以解决这个问题。
    
    
* 在idea的console 中执行git log 的时候，出现中文乱码


    在解决了cmd 中执行git的中文乱码之后，调用 idea 中的console，依然还有乱码问题，通过查看idea 中
    console中的lang 变量，发现没有定义这个变量。因此 这里通过修改idea 中console 调用的console来解决，
    之前调用window的cmd发现没有解决文件，后来切换为git自带的git-bash.exe 将问题解决了。
    
    设置方法：
    File--》 setting ----》Tools---》Terminal 来设置Shell path 的取值为git安装目录下的 C:\Program Files\Git\git-bash.exe

    参考资料：
    https://blog.csdn.net/qq_32454537/article/details/82107998


*  当使用git stash apply 恢复储藏的时候，有些情况下，可能会造成冲突，这种情况的解决方法：
    
    
	方法一： 如果编辑了默写文件之后，发现该分支存在一个stash 和该文件有关，此时执行 git stash apply，会造成冲突，
	打开文件可以发现在文件中有一些冲突信息，其中Updated upstream 和=====之间的内容就是pull下来的内容，====和stashed changes之间的内容就是本地修改的内容。
	在这种情况下，因为 stash 没有完全正确的恢复，因此，造成了一些问题，导致stash 列表中的stash没有消失 (执行执行stash list 的时候，仍然可以查询到之前恢复的那个stash)
	此时，正确的做法是，编辑冲突文件，根据自己的需要，解决冲突，然后将文件提交，之后执行 git stash drop <stash@{id}> 将stash从stash 列表中删除 。
	    	
==
	
    在开发到一半的时候，发现了该分支下有一个stash储藏，但是此时还没有执行 git stash apply 命令，但是我们知道此时一定会产出冲突，解决方法
	方法一： 执行 git stash apply ，安装上面提到的方法来结局
	方法二(从储藏中创建分支)： 执行 git stash branch 分支名A  命令，将stash创建成一个分支，安装分支冲突的解决方法来解决  

==    



* 在window下创建.gitignore 文件的小技巧
打开git-bash ， 执行  touch .gitignore 文件即可。 
