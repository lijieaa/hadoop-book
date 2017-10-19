# 1.修改主机名（IP变换不用修改配置文件，也方便记性各主机有哪些节点）

\#**临时修改主机名**

**hostname hadoop0     **

**\#永久修改主机名**

* **vi /etc/sysconfig/network                
  **

* **HOSTNAME=localhost.localdomain  \#修改localhost.localdomain为hadoop0                
  **

* **vi /etc/hosts                
  **

* **127.0.0.1    localhost.localdomain  \#修改localhost.localdomain为hadoop0                
  **

* **reboot**

# 2.节点规划

| 192.168.212.130（hadoop0） | 192.168.212.131\(hadoop1\) | 192.168.212.132\(hadoop2\) |
| :--- | :--- | :--- |
| NameNode | ResourceMannager | SecondaryNameNode |
| DataNode | DataNode | DataNode |
| NodeManager | NodeManager | NodeManager |

# 3.slaves配置

hadoop0

hadoop1

hadoop2

# 4.hdfs-site.xml配置

**&lt;configuration&gt;          
**

**  &lt;property&gt;          
**

**    &lt;name&gt;dfs.namenode.secondary.http-address&lt;/name&gt;          
**

**    &lt;value&gt;hadoop2:50090&lt;/value&gt;          
**

**  &lt;/property&gt;          
**

**&lt;/configuration&gt;**

# 5.配置SSH免密码登录

**ssh-copy-id hadoop1**

**ssh-copy-id hadoop2**

**ssh hadoop1**

**ssh hadoop2**

# 6.重新格式化文件系统

**hdfs namenode -format**

7.



