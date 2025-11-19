# <center>Redis</center>  

开启临时服务：cmd目录，启动临时服务 redis-server.exe redis.windows.conf  

连接服务：cmd目录，进行客户端调用  redis-cli.exe -h 127.0.0.1 -p 6379  

安装Redis Windows服务：
redis-server.exe --service-install redis.windows.conf --service-name redisserver --loglevel verbose  

启动服务：redis-server.exe --service-start --service-name redisserver  

停止服务：redis-server.exe --service-stop --service-name redisserver  

卸载服务：redis-server.exe --service-uninstall--service-name redisserver  

设置密码：redis.windows.conf 文件中 requirepass 处 lunatic  

连接服务: cmd目录，redis-cli.exe 输入auth lunatic  