Supported devices: A8(X) - A11, iOS 14.0 - 15.5b4

Video tutorial: https://youtu.be/SsvumuaZBT0

Run git clone https://github.com/verygenericname/SSHRD_Script --recursive && cd SSHRD_Script

Run ./sshrd.sh https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw TrollStore Tips

Enter the device into DFU mode according to the prompt or enter DFU mode in advance

Firmware address：https://ipsw.me/ Choose your own device firmware link to replace the above https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw

Run ./sshrd.sh boot the device should start verbosing and show a TrollFace in ascii, then reboot eventually

Open up the app you replaced, it should be TrollStore Helper now

Press "Install TrollStore", make sure you're connected to the internet

Done, your device will respring and TrollStore should appear on your home screen

Note: The phone language is set to English, the computer must be over the wall and Xcode and Command Line Tools must be installed. The installation command is as follows: xcode-select --install
