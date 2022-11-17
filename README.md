# 我的vps都做了什么

## 梯子
### 工具
- 系统:ubuntu 18.04
- 服务器:caddy
- 代理协议:trojan-go
- BBR加速
### BBR加速
修改系统变量：
```
echo net.core.default_qdisc=fq >> /etc/sysctl.conf
echo net.ipv4.tcp_congestion_control=bbr >> /etc/sysctl.conf
```
保存生效:
```
sysctl -p
```
执行:
```
sysctl net.ipv4.tcp_available_congestion_control
```
执行结果：
```
sysctl net.ipv4.tcp_available_congestion_control
net.ipv4.tcp_available_congestion_control = bbr cubic reno
```
查看是否生效：
```
lsmod | grep bbr 
```
### caddy
### 代理协议


