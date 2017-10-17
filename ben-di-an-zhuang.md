1.创建目录放置软件

mkdir opt

2.解压JDK

tar -zxvf jdk-8u144-linux-x64.tar.gz -C opt

3.更改jdk1.8.0\_144目录名为jdk8（目录名太长不好记性）

cd opt

mv jdk1.8.0\_144/ jdk8

4.配置JAVA\_HOME环境变量

su root   切换到root用户

vim /etc/profile

export JAVA\_HOME=/home/vsz/opt/jdk8

export PATH=$PATH:$JAVA\_HOME/bin

source /etc/profile

java -version

5.解压hadoop

tar -zxvf hadoop-2.5.0.tar.gz -C opt/

mv hadoop-2.5.0/ hadoop

6.本地运行



