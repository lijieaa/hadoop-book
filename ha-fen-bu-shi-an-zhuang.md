# 1.hdfs-site.xml配置

**&lt;configuration&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.nameservices&lt;/name&gt;              
**

**    &lt;value&gt;mycluster&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.ha.namenodes.mycluster&lt;/name&gt;              
**

**    &lt;value&gt;nn1,nn2&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.namenode.rpc-address.mycluster.nn1&lt;/name&gt;              
**

**    &lt;value&gt;hadoop0:8020&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.namenode.rpc-address.mycluster.nn2&lt;/name&gt;              
**

**    &lt;value&gt;hadoop1:8020&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.namenode.http-address.mycluster.nn1&lt;/name&gt;              
**

**    &lt;value&gt;hadoop0:50070&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.namenode.http-address.mycluster.nn2&lt;/name&gt;              
**

**    &lt;value&gt;hadoop1:50070&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.namenode.shared.edits.dir&lt;/name&gt;              
**

**    &lt;value&gt;qjournal://hadoop0:8485;hadoop1:8485;hadoop2:8485/mycluster&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.journalnode.edits.dir&lt;/name&gt;              
**

**    &lt;value&gt;/home/vsz/opt/hadoop/tmp/data&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.client.failover.proxy.provider.mycluster&lt;/name&gt;              
**

**    &lt;value&gt;org.apache.hadoop.hdfs.server.namenode.ha.ConfiguredFailoverProxyProvider&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.ha.fencing.methods&lt;/name&gt;              
**

**    &lt;value&gt;sshfence&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**              
**

**  &lt;property&gt;              
**

**    &lt;name&gt;dfs.ha.fencing.ssh.private-key-files&lt;/name&gt;              
**

**    &lt;value&gt;/home/vsz/.ssh/id\_dsa&lt;/value&gt;              
**

**  &lt;/property&gt;              
**

**&lt;/configuration&gt;**

# 2.core-site.xml配置

**&lt;configuration&gt;          
**

**  &lt;property&gt;          
**

**    &lt;name&gt;fs.defaultFS&lt;/name&gt;          
**

**    &lt;value&gt;hdfs://mycluster&lt;/value&gt;          
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

# 3.同步配置文件

**scp opt/hadoop/etc/hadoop/\*.xml opt/hadoop/etc/hadoop/slaves hadoop1:/home/vsz/opt/hadoop/etc/hadoop/**

**scp opt/hadoop/etc/hadoop/\*.xml opt/hadoop/etc/hadoop/slaves hadoop2:/home/vsz/opt/hadoop/etc/hadoop/**

# 4.启动journalnode\(至少启动3个节点\)

**hadoop-daemon.sh start journalnode**

# 5.格式化hdfs文件系统

**hdfs namenode -format**

# 6.启动第一个NameNode\(hadoop0\)





