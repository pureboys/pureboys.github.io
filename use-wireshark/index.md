# Linux普通用户使用Wireshark的权限不足的问题


### 解决方法

1. 将dumpcap更改为Wireshark用户组
```
sudo chgrp wireshark /usr/bin/dumpcap
```

2. 让Wireshark用户组有root权限使用dumpcap
```
sudo chmod 4755 /usr/bin/dumpcap
```

3. 将自己加入Wireshark用户组,我的用户是 abc ,你添加需要更改这个
```
sudo gpasswd -a abc wireshark
```
