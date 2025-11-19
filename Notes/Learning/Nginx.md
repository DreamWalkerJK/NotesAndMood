# <center>Nginx</center>  
8081 端口80   

进入nginx容器中，查看nginx配置内容  
> docker exec -it nginx /bin/bash

看配置文件  
> cd /etc/nginx/nginx.conf   

退出  
> exit  

执行命令，创建www、logs、conf 三个文件
> mkdir -p /root/nginx/www /root/nginx/logs /root/nginx/conf  

查看nginx容器id  
> docker ps  

拷贝到本地  
> docker cp 容器id:/etc/nginx/conf.d/default.conf /root/nginx/conf