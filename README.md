这分别是windows和linux下的lcx
代码来源于网络，并不是我自己写的，很长时间了已经找不到来源了，故无法添加来源，向作者致歉
##windows下

##linux下
编译
```
gcc linux_lcx.c -o lcx
```
####用法
```
[root@localhost]:~# ./lcx
Socket data transport tool
by bkbll(bkbll@cnhonker.net)
Usage:./lcx -m method [-h1 host1] -p1 port1 [-h2 host2] -p2 port2 [-v] [-log filename]
 -v: version
 -h1: host1
 -h2: host2
 -p1: port1
 -p2: port2
 -log: log the data
 -m: the action method for this tool
 1: listen on PORT1 and connect to HOST2:PORT2
 2: listen on PORT1 and PORT2
 3: connect to HOST1:PORT1 and HOST2:PORT2
Let me exit...all overd
```
列举两个常用的
端口反弹（将A端口的数据统统发送到B端口）
```
./lcx -m 2 -p1 5555 -p2 6666
```
端口转发（连接到A主机的A端口，数据发送到B主机的B端口）
```
./lcx -m 3 -h1 1.1.1.1 -p1 5555 -h2 2.2.2.2 -p2 6666
```
