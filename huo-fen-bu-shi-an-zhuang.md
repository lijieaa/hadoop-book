# 1.core-site.xml配置

**&lt;configuration&gt;                                          
**

**  &lt;property&gt;                                          
**

**    &lt;name&gt;fs.defaultFS&lt;/name&gt;                                          
**

**    &lt;value&gt;hdfs://localhost:9000&lt;/value&gt;                                          
**

**  &lt;/property&gt;                                          
**

**  &lt;property&gt;                                          
**

**    &lt;name&gt;hadoop.tmp.dir&lt;/name&gt;                                          
**

**    &lt;value&gt;/home/vsz/opt/hadoop/tmp&lt;/value&gt;                                          
**

**  &lt;/property&gt;                                          
**

**&lt;/configuration&gt;**

# 2.hdfs-site.xml配置

**&lt;configuration&gt;                                      
**

**  &lt;property&gt;                                      
**

**    &lt;name&gt;dfs.replication&lt;/name&gt;                                      
**

**    &lt;value&gt;1&lt;/value&gt;                                      
**

**  &lt;/property&gt;                                      
**

**&lt;/configuration&gt;**

# 3.配置ssh免密码登录

**ssh-keygen -t dsa -P '' -f ~/.ssh/id\_dsa**

**ssh-copy-id localhost**

**ssh localhost**

# 4.格式式文件系统

**bin/hdfs namenode -format**

# 5.修改hadoop-env.sh脚本里JAVA\_HOME路径

**export JAVA\_HOME=/home/vsz/opt/jdk8/**

# 6.启动NameNode和DataNode守护进程

**sbin/start-dfs.sh**

**jps**

**出现如下进程，启动成功，如图：**

**DataNode**

**SecondaryNameNode**

**NameNode**

# 7.通过WEB-UI（[http://192.168.212.130:50070/）查看NameNode状态，如果除本机以外不能访问，请关闭防火墙](http://192.168.212.130:50070/）查看NameNode状态，如果除本机以外不能访问，请关闭防火墙)

**service iptables stop **

**chkconfig iptables off**

**service iptables status**

# 如图：![](/assets/50070.png)8.yarn框架配置

## 8.1配置mapred-site.xml

**&lt;configuration&gt;      
**

**    &lt;property&gt;      
**

**        &lt;name&gt;mapreduce.framework.name&lt;/name&gt;      
**

**        &lt;value&gt;yarn&lt;/value&gt;      
**

**    &lt;/property&gt;      
**

**&lt;/configuration&gt;**

# 8.2 配置yarn-site.xml

**&lt;configuration&gt;        
**

**    &lt;property&gt;        
**

**        &lt;name&gt;yarn.nodemanager.aux-services&lt;/name&gt;        
**

**        &lt;value&gt;mapreduce\_shuffle&lt;/value&gt;        
**

**    &lt;/property&gt;        
**

**&lt;/configuration&gt;**

# 8.3 启动yarn,通过WEB-UI（http://192.168.212.130:8088）查看YARN状态，如图：![](/assets/8088.png)



