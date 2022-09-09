1.下载开源中的TrollStore.tar文件，链接：https://github.com/opa334/TrollStore/releases/tag/1.0.7

2.运行 git clone https://github.com/verygenericname/SSHRD_Script --recursive && cd SSHRD_Script

3.运行 ./sshrd.sh <此处为固件下载链接>
例子：./sshrd.sh https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw
固件链接可以去这个网站根据自己的设备获取：https://ipsw.me/
根据提示将设备进入DFU模式

4.等待上一步运行完成输入./sshrd.sh boot回车等待设备进去代码模式，如何出现失败请多次运行./sshrd.sh boot并将设备进入到DFU模式，直到成功
 
5.打开一个新的SSH窗口输入iproxy 2222 22回车

6.回到之前的SSH窗口输入ssh -p2222 root@localhost回车，根据提示输入密码回车，默认密码alpine

7.运行：mount_filesystems等待完成

8.运行：find /mnt2/containers/Bundle/Application  -name Tips回车显示Tips完整信息，找到以后把UDID复制出来保存可进入下一步，输入cd /mnt2/containers/Bundle/Application 再次输入cd 8872BC29-420D-4091-AF61-838003B48470/Tips.app,即可进行下一步

9.运行cd /mnt2/containers/Bundle/Application/7DC22AEE-4325-43B8-939A-B49EF1CF903D/Tips.app回车，再次运行mv Tips Tips.backup回车

10.重新打开一个SSH窗口找到第1步下载的文件解压目录cd进入app目录
例子：cd ~/Downloads/TrollStore.app
运行：scp -P2222 PersistenceHelper root@localhost:/mnt2/containers/Bundle/Application/8872BC29-420D-4091-AF61-838003B48470/Tips.app/Tips 
再次运行：scp -P2222 trollstorehelper root@localhost:/mnt2/containers/Bundle/Application/8872BC29-420D-4091-AF61-838003B48470/Tips.app/trollstorehelper

11.回到第一个SSH窗口
运行：chown 33 Tips & chmod 755 Tips trollstorehelper & chown 0 trollstorehelper 回车

12.输入reboot重启设备

13.进入系统打开Tips就可以进行安装TrollStore
