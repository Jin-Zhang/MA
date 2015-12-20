### Flood algorithm

Flood algorithm is used to find out the direct connected device of the client.

洪水查询 算法用于寻找 客户端 直接相连 的设备。

#### Configurations

1. **devices.json** Stores the device list of the network.

device = {

}

2. **config.json** 

first_hop_ip: 第一跳IP 地址

root_device: The name of the root device( router/ switch) 根路由器的名字

It must be as same as one of the devices.

#### Flooding

1. **Generate mac-device-dict**

dict 意思是字典，即 键值对 变量。

MAC-device-dict is used to faster the query from MAC to device.
地址 设备 字典用于加快从 地址 到 设备 的查询。

While generating the mac-device-dict, MAC address should be converted to _long_ format. MAC address is stored as _string_ format for easy readable. But in the program, string format is not easy to compare with because of the _case sensive comparasion_, different format( splitted by : . or -) or encoding problem (Unicode or ASCII).

2. **Generate the network topology structure**

生成网络拓扑结构

The devices are stored as list, but the actual network should be organized as a tree, that's why it should be converted to another topology structure.

3. **Recursive search**

递归查询

Search the topology tree recursivly. 

一个节点有以下状态：
* 可查询（Support SNMP）
* 是否含有子节点 - 如果在devices 中定义有子节点，但是刷不到其IP地址，也无法查询。
* IP 是否与查询目标相同
* 

> For each node of the tree:  
>   if it's IP == the target client:
>     if it contains no sub node:
>       found, return
>   else:
>   

递归搜索拓扑树，对树上的每个节点：

遇到的问题：

1. 每个设备的表现都很不一样，除了两台MAC  
2. 配置Linux 下的Router 遭遇困难，后来发现无线网卡不支持  
3. ASUSWRT 和OPEN Wrt 总是编译不成功  
4. pfctl 非常麻烦  
5. switch 总是刷不到IP  
6. 设备延迟严重，重复实验难以获得相同结果  