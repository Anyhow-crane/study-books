## linux CentOS-7 安装

> 虚拟机VMware ,CentOS-7-Minimal最小版本,网络选择NAT模式,默认安装.

1. 安装完成登录后无法联网

```shell
#选择root用户
su
#修改配置文件(ifcfg-ene32不一定一样,en开头的就是的了)
cd /etc/sysconfig/network-scripts
#将 ONBOOT=no 改为 ONBOOT=yes(最小版本没有vim)
vi ifcfg-ene32
#重启网卡
service network restart
#查看网络(没有ifconfig)
ip addr
ping www.baidu.com
#安装网络工具(如ifconfig)
yum -y install net-tools
```

2. 普通用户获取sudo权限

* 安装时添加用户的时候选择创建管理员
* 使用命令

>1. 切换root用户,运行visudo命令
>2. 添加xxx ALL=(ALL) ALL,(xxx为用户名)

```shell
su
visudo
## i 添加后退出 esc :wq
exit
```

3. 更新

```shell
sudo yum update
```

