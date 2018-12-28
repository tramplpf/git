#git 中的日志查看
* 查看某个文件的commit 提交记录

 
    git log --pretty=oneline todo/todo.md

    git log --pretty=oneline  , git log --oneline , git log --pretty=one 三者的效果一样。 
    
    
# 让git 记录按照图形的形式展示历史记录(仓库可视化)
    
    git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative

--graph 选项将图表添加到日志的左侧， --abbrev-commit 存储提交使用了 SHA 方法， --date=relative 表达式用相对的术语来表示日期，
并且 --pretty 以 bit 格式处理自定义格式。



查看某个文件的提交记录以及对此文件的修改

    git log -p 文件名
         
