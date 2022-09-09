1. Download the TrollStore.tar file in open source, link: https://github.com/opa334/TrollStore/releases/tag/1.0.7

2. Run git clone https://github.com/verygenericname/SSHRD_Script --recursive && cd SSHRD_Script

3. Run ./sshrd.sh <firmware download link here>
Example: ./sshrd.sh https://updates.cdn-apple.com/2022SummerFCS/fullrestores/012-52889/B5338EBD-ED5C-4637-A829-6A269A2BD916/iPhone_5.5_P3_15.6.1_19G82_Restore.ipsw
The firmware link can go to this website to obtain according to your own device: https://ipsw.me/
Put the device into DFU mode as prompted

4. Wait for the previous step to complete and enter ./sshrd.sh and press Enter to wait for the device to enter the code mode. If it fails, please run ./sshrd.sh multiple times and enter the DFU mode until it succeeds.
 
5. Open a new SSH window and enter iproxy 2222 22 Enter

6. Go back to the previous SSH window and enter ssh -p2222 root@localhost and press Enter, enter the password according to the prompt and press Enter, the default password is alpine

7. Run: mount_filesystems and wait for completion

8. Run: cd /mnt2/containers/Bundle/Application and press Enter, enter ls to view the program UDID list, the program name (UDID is displayed) will not be displayed here, only cd to the directory and enter ls to view
Example: cd /mnt2/containers/Bundle/Application/UDID Enter ls and press Enter to view the name. According to the author's suggestion, it is best to use Tips, which is to prompt this APP
Here you can only find it out in a fool-like operation. After you find it, copy the UDID and save it to go to the next step.
 
Or enter find/mnt2/containersl/Bundle/Application f -name Tips and press Enter to display the complete Tips information. After finding it, copy the UDID and save it to go to the next step (you can omit cd /mnt2/containers/Bundle/Application, enter ls to view the program UDID list, the program name will not be displayed here (UDID is displayed), you can only cd to the directory and enter ls to view
Example: cd /mnt2/containers/Bundle/Application/8872BC29-420D-4091-AF61-838003B48470 press Enter, enter ls and press Enter to view the name), copy the UDID and save it after finding it, and then go to the next step

9. Run cd /mnt2/containers/Bundle/Application/UDID/Tips.app and press Enter, then run mv Tips Tips.backup and press Enter again

10. Re-open an SSH window, find the file downloaded in step 1, unzip the directory, and cd into the app directory
Example: cd ~/Downloads/TrollStore.app
Run: scp -P2222 PersistenceHelper root@localhost:/mnt2/containers/Bundle/Application/UDID/Tips.app/Tips
Run again: scp -P2222 trollstorehelper root@localhost:/mnt2/containers/Bundle/Application/UDID/Tips.app/trollstorehelper

11. Go back to the first SSH window
Run: chown 33 Tips & chmod 755 Tips trollstorehelper & chown 0 trollstorehelper Enter

12. Enter reboot to restart the device

13. Enter the system and open Tips to install TrollStore
