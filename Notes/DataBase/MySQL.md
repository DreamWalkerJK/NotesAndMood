# <center>MySQL</center>  

mysql 初始化root密码： (3am-5eszvZ&  
更改后的密码：lunatic  

下载mysql：Download->MySQL Community(GPL) Downloads
->MySQL Community Server->...ZIP Archive（免安装版）  

配置mysql：  
0、以管理员的身份打开命令行  
1、转到mysql的bin目录  
2、初始化mysql（mysqld --initialize --console）  
3、启动mysql服务：net start mysql  
4、登录命令： mysql -u root -p  
5、修改密码：alter user 'root'@'localhost' identified by '新的密码'  
6、结束：exit  

为了方便登录，设置全局变量：  
0、我的电脑-->属性-->高级系统设置-->环境变量  
1、新建系统变量（变量名：mysql 变量值：mysql安装目录）  
2、编辑Path路径变量，新建（%mysql%\bin）->确定  
3、在mysql目录下创建一个ini/cnf配置文件，命名my.ini  
[mysqld]  
character-set-server=utf8mb4  
bind-address=0.0.0.0  
port=3306  
default-storage-engine=INNODB  
[mysql]  
default-character-set=utf8mb4  
[client]  
default-character-set=utf8mb4  

命令参考：  
0、安装服务：mysqld --install  
1、初始化：　mysqld --initialize --console  
2、开启服务：net start mysql  
3、关闭服务：net stop mysql  
4、登录mysql：mysql -u root -p  
5、修改密码：alter user 'root'@'localhost'   identified by 'root';(by 接着的是密码)  
6、标记删除mysql服务：sc delete mysql  