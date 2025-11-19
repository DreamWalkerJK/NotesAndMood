# <center>Docker</center>   

设置开机启动
> sudo systemctl start docker  
sudo systemctl enable docker  

关机  
> sudo systemctl disable docker  

容器设置自动启动  
> docker run -d -p 9090:9090 --restart=always --name mytomcat tomcat  

已运行，容器启动时没有设置  
> docker update --restart=always 容器名或者id  

取消容器开机自启  
> docker update --restart=no 容器名或者id // no是默认值  

重启docker服务  
>sudo systemctl daemon-reload  
sudo systemctl restart docker  