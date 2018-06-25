## ssh指令

**拷贝文件**：拷贝文件到指定服务器的指定路径下，指定端口-P要放置到scp后，且为大写的P

```shell
#本机拷贝文件到服务器
scp -P 9090 KDUMClient.war root@192.168.12.48:/home/kingdom/cz_publicserver_8085/webapps
#服务器拷贝文件到本机
scp -P 9090 root@192.168.12.48:/home/kingdom/cz_pdaserver_8083/logs/catalina.out /Users/xd/Desktop/
```

**查看端口占用情况：**

```Shell
#所有端口
lsof
#分页展示
lsof | less
#查看指定端口
lsof -i:3000
```

