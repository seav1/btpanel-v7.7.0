# btpanel-v7.6.0
btpanel-v7.6.0-backup  官方原版v7.6.0版本面板备份

**Centos/Ubuntu/Debian安装命令 独立运行环境（py3.7）**

```Bash
curl -sSO https://raw.githubusercontent.com/seav1/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```

添加nat 64
```Bash
echo -e "nameserver 2001:67c:2b0::4\nnameserver 2001:67c:2b0::6" > /etc/resolv.conf
```

降级到7.6

添加nat 64
```Bash
wget https://github.com/wei/baota/releases/download/7.6.0/LinuxPanel-7.6.0.zip
```
```Bash
unzip LinuxPanel-7.6.0.zip
```
```Bash
cd panel/
```

```Bash
bash update.sh
```

开启宝塔支持ipv6
```Bash
echo "True" > /www/server/panel/data/ipv6.pl
bt reload
```

删除手机绑定
```Bash
rm -f /www/server/panel/data/bind.pl
```

