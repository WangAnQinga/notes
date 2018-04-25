1. 进入ubuntn系统，可以看到ubuntu系统的版本信息,如下：

```
    Welcome to Ubuntu 16.04.4 LTS (GNU/Linux 4.4.0-105-generic x86_64)

    * Documentation:  https://help.ubuntu.com
    * Management:     https://landscape.canonical.com
    * Support:        https://ubuntu.com/advantage

    Welcome to Alibaba Cloud Elastic Compute Service !

    Last login: Wed Apr 25 14:52:45 2018 from 127.0.0.1
    
```
2. > apt-get update  更新软件源中的所有软件列表 

3.  安装软件命令 app-get install   例如：
    安装node： ``` apt-get install nodejs  ``` 
    安装npm： ``` apt-get install npm  ``` 
    需要升级node和npm，利用npm模块n，运行命令 ``` npm install -g n ```，然后运行 ``` n stable / n latest ``` ，然后运行 ``` node -v / npm -v ``` 发现还是原来的版本，为什么 n stable / n latest不生效？为啥呢？ 答案：你需要重新进入linux服务器，再次运行 ``` node -v/npm -v ```，发现node 就是稳定或者最新版本了

4.  ssh 链接不断线问题？  
    修改 /etc/ssh/sshd_config 文件. ``` vi /etc/ssh/sshd_config  ```
    (1) 添加  ``` ClientAliveInterval 60  ClientAliveCountMax 1 ```  
    (2)重启ssh服务  ``` service ssh restart  ```  
    注意事项：需要重新进去服务器才会生效

5.  安装 pm2  ``` npm install -g pm2 ```