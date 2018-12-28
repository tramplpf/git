# 网络上关于git 的一些错误的理解

网络上说git reset --hard commit_tid 可以实现对文件回退，无法再回来，经过自己的测试，只要你之前通过 git log --pretty=oneline 命令查看当前commit 的id ，然后，在通过 git reset --hard 新的commit ； 
这里当然也可以通过 git reflog 命令查看HEAD 指针的移动情况来确定HEAD 所执行的COMMIT ID; 




