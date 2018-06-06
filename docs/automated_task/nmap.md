## 存活探索

  探测内部网络中的存活设备


## 探测协议

  首先了解一下，需要探测的协议：

![探测协议](../asset/assets_scanning/探测协议.png)

## 探测模块和工具

nmap - 是一款用于网络发现和安全设计的让利安全工具

nmap模块，在系统环境下的安装：


```
yum install nmap

```


nmap模块，在python环境下的安装：


```
pip install python-nmap

```


## nmap工具在系统环境中使用


```
$ nmap -n -sP -PE 192.168.199.214
```
>参数说明：
>
> -n : 不对目标机器的ip地址反解析
>
>-sP: icmp协议探测
>
> -PE: tcp协议探测

## python-nmap在python环境的使用

```

import nmap

nm = nmap.PortScanner()

nm.scan(hosts='192.168.199.214', ports=None, arguments='-n -sP -PE')
# 获取启用存活的主机列表
ret = nm.all_hosts()

print(ret)

```
