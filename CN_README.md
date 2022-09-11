教程开源地址：https://github.com/Patickhuang/TrollStore.git
A8-A11设备15.0-15.5b4系统无须越狱安装TrollStore永久签名个人整理傻瓜式操作，本人操作环境是MAC系统

视频教程：https://www.youtube.com/watch?v=SsvumuaZBT0

1.运行 git clone https://github.com/verygenericname/SSHRD_Script --recursive && cd SSHRD_Script

2.运行 ./sshrd.sh https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw TrollStore Tips
根据提示将设备进入DFU模式或提前进入DFU模式

固件地址：https://ipsw.me/  自行选择自己的设备固件链接替换上面的https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw

3.等待上一步运行完成输入./sshrd.sh boot回车等待设备进入代码模式，如何出现失败请多次运行./sshrd.sh boot并将设备进入到DFU模式，直到自动重启方可成功
 

注意事项：手机语言设定为英文，电脑必须翻墙和安装Xcode并安装Command Line Tools,安装命令如下： xcode-select --install
