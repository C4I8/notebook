# DOS 命令
ECHO 显示字符串  
IF EXIST 文件/文件夹 判断文件/文件夹是否存在  
IF "STR" == "STR" 判断字符串是否相等  
IF 0 EQU 0 判断 数值是否相等  
IF DEFINE STR 判断变量是否定义  
在命令行末尾输入"^"实现换行输入 或者 用(\n)实现换行
<BR>
查看指定端口的使用情况

    netstat -ano | findstr 端口号
手动关闭进程

    taskkill -PID 进程号 -F