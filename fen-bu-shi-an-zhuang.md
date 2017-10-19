# 1.修改主机名（IP变换不用修改配置文件，也方便记性各主机有哪些节点）

\#**临时修改主机名**

 **hostname hadoop0     **

**\#永久修改主机名**

* **vi /etc/sysconfig/network  **

* **HOSTNAME=localhost.localdomain  \#修改localhost.localdomain为hadoop0  **

* **vi /etc/hosts  **

* **127.0.0.1    localhost.localdomain  \#修改localhost.localdomain为hadoop0  **

* **reboot**



