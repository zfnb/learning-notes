### 简介

-  每一个网卡都有一个6 字节（48bit的地址（ Media Access Control Address） 

- 全球唯一，固化在了网卡中，由IEEE802标准规定

- 前3字节： OUI组织唯一标识符 

-  后3字节：网络接口标识符 ,由厂商自行分配 


### 地址的表示格式
- windows 
  + 40-55-82-0A-8C-6D
-  Linux、Android、Mac、iOS 
  + 40:55:82:0A:8C:6D 

### MAC地址操作

- 查看mac地址：ipconfig /all
- 修改mac地址
  - 更改适配器选项 - 属性 -  配置 - 高级 - 网络地址
### MAC地址的获取
- 当不知道对方主机的MAC地址时，可以通过ARP广播协议获取对方的MAC地址
   + 获取成功后，会缓存ip地址，MAC地址的映射信息，俗称ARC缓存
   + 通过ARP广播获取的MAC地址，属于动态缓存，存储时间比较短(默认两分钟)，过期自动删除
- ARP ：地址解析协议，用于通过IP地址获取MAC地址
- 相关指令
   + arp -a [主机地址]：查询ARP缓存
   + arp -d [主机地址]：删除ARP缓存
   + arp -s 主机地址 MAC地址：增加一条缓存(静态缓存，存储时间较久)