### 端口的探测
通过nmap工具可以探测存活的主机列表。下面我们通过telnetlib工具，从主机列表中通过探测端口是否是Linux服务器

### SSH 探测流程

![探测过程](探测过程.png)



### 端口探测

> telnet:是系统中，判断端口是否存活命令
>
> telnetlib模块:python中的 判断端口的存活以及返回结果的模块


```
$ telnet 192.168.199.214
```

python 环境中探测端口

```
import telnetlib
tm = telnetlib.Telnet(host='192.168.199.214', port='22', timeout=4)
ret = tm.read_until('\n', timeout=5)
print(ret)

```

### 总结

![探测存活ip列表以及服务器主机](探测原理.png) 
