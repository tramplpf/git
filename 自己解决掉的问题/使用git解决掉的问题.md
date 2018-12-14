# 使用git 解决掉的问题

安装好git之后，在正常的命令行下面执行git log 命令也为出现中文乱码现象。
    通过设置环境变量 LANG 的取值为 zh_CN.UTF-8 可以解决这个问题。
在idea的console 中执行git log 的时候，出现中文乱码
    在解决了cmd 中执行git的中文乱码之后，调用 idea 中的console，依然还有乱码问题，通过查看idea 中
    console中的lang 变量，发现没有定义这个变量。因此 这里通过修改idea 中console 调用的console来解决，
    之前调用window的cmd发现没有解决文件，后来切换为git自带的git-bash.exe 将问题解决了。
    
    设置方法：
    File--》 setting ----》Tools---》Terminal 来设置Shell path 的取值为git安装目录下的 C:\Program Files\Git\git-bash.exe

    参考资料：
    https://blog.csdn.net/qq_32454537/article/details/82107998

