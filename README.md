# 小米路由器3G刷老毛子固件

> 最近把服役三四年的小米路由器mini换成了3G, 到手就刷了老毛子固件, 把过程与备份放这边 

### 准备FAT/FAT32格式U盘一枚

### 刷开发版ROM

* [下载ROM](http://www1.miwifi.com/miwifi_download.html)

* 将ROM重命名为`miwifi.bin`拷贝到U盘中, 插入路由器

* 按住reset按钮之后重新接入电源, 指示灯变为黄色闪烁状态即可松开reset键

### 开启SSH

* 下载[工具](http://www1.miwifi.com/miwifi_open.html)

* 将工具重命名为`miwifi_ssh.bin`, 操作同上

### 刷Breed Bootloader

* [下载](https://breed.hackpascal.net/)

* 拷贝`breed.bin`至路由器

  ```
  scp breed.bin root@192.168.31.1:/tmp/
  ```

* 登录路由器, 刷入Breed

  ```
  ssh root@192.168.31.1
  
  ********
  
  mtd -r write /tmp/breed.bin Bootloader
  ```
  
### 进入Breed

* 按住reset按钮之后重新接入电源, 闪烁松开

* 访问[192.168.1.1](http://192.168.1.1)

### 备份固件

* EEPROM

* 编程器固件


### 刷入老毛子固件

* 下载[paddavan](http://opt.cn2qq.com/padavan/)

* Breed -- 固件更新 -- 选择刷入

* 访问[后台](http://192.168.123.1)

