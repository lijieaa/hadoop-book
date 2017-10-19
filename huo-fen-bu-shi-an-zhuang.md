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



# 6.启动NameNode和DataNode守护进程



