# <center>RabbitMQ</center>  
端口：http://localhost:15672 

用户名&密码：guest  
admin lunatic  

RabbitMQ的sbin目录打开CMD执行安装：  
> rabbitmq-plugins enable rabbitmq_management

CMD管理员身份运行  
> net start RabbitMQ  启动  
net stop RabbitMQ  停止  
rabbitmqctl status  查看状态  

健康检查： rabbitmqctl status  
启动监控管理器：rabbitmq-plugins enable rabbitmq_management  
关闭监控：rabbitmq-plugins disable rabbitmq_management  
停止服务：rabbitmq-service stop  
启动服务：rabbitmq-service start  
重启命令：net stop RabbitMQ && net start  
帮助命令：rabbitmqctl help  

> rabbitmqctl list_queues查看所有队列  
rabbitmqctl reset清除所有队列  
rabbitmqctl list_exchanges查看所有交换器  
rabbitmqctl add_user username password添加用户  
rabbitmqctl set_user_tags username administrator分配角色  
rabbitmqctl list_bindings 查看交换器和队列的绑定关系  

-- 用户 root root123456  
创建 admin 用户并指定密码:  
> rabbitmqctl add_user admin adminli  

设置 admin 用户读写所有队列的权限:  
> rabbitmqctl set_permissions admin ".*" ".*" ".*" 

设置 admin 用户所属的用户组:  
> rabbitmqctl set_user_tags admin administrator  

查看用户列表：  
> rabbitmqctl list_users  

修改 admin 用户的密码为 admin123：  
> rabbitmqctl change_password admin admin123  

删除 admin 用户：  
> rabbitmqctl delete_user admin  

