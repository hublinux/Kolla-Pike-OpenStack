准备硬件环境
新创建 3 台虚拟机，分别作为 controller 节点，compute 节点，storage 节点。其中 controller
节点 2 张网卡，compute、storage 节点各 1 张网卡。操作系统为 centos7.5
主机名  IP 角色 内存 网卡类型
test01 192.168.10.101 controller 节点 8G ens33 和 ens38 都桥接
test02 192.168.10.103 compute 节点 4G ens33 桥接
test03 192.168.10.102 storage 节点 4G ens33 桥接
注：每个主机的 ens33 网卡作为内部管理 openstack 的网络和 web 界面的网络接口。 controller
节点的 ens38 网卡作为 对外的 网络。 compute 和 storage 一张即可，因为丌需要 tunnel 网络，直
接使用 1 个网卡。
