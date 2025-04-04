# Convert China Version to Global Version

## Make Sure You Already Backup Your Partition

### `--noreconnect` is required for Windows, no need for Linux

## Tools:
1. [Download GongChengROM](https://xiaoai.qgmzmy.me/d/lx04/rom/%E5%B7%A5%E7%A8%8Brom/GongChengROM.zip?sign=XUYpVHg_ulRWQxfyrwZo-RZP0H-T70XXk7jV9n3OkHA=:0)
2. [Global Dump ROM Dump_mico_x04g.tar.xz](https://archive.org/details/dump_mico_x04g)
3. [SP Flash Tool](https://spflashtool.com/download/)
4. [Hikaru_resign-Xiaomi](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/Hikaru_resign-Xiaomi.7z)
5. [gpt_x04g.bin](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/files/gpt_x04g.bin)
6. [boot1_for_microx04g.bin](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/files/boot1_for_microx04g.bin)

# Guide:

## 1. **Flash GongChengROM with FlashTool**  
   Set all path to same to the screenshot
   ![image](https://github.com/user-attachments/assets/870fe5e8-da0a-43ce-b372-e8645a4f824e)  
   
   If you booted it on the latest batch, it may glitch.  
   Don’t worry, it won’t break. It's just missing a driver, and we don’t need the display driver to rewrite the MAC.
   <img src="https://github.com/user-attachments/assets/4730eb94-54ba-4236-bef7-24e65e36323b" alt="image" width="300"/>

## 2. **Unplug the Device, Open SN_Write_Tool, and Set It to Match the Picture**  
   ![image](https://github.com/user-attachments/assets/b644ffb7-0f60-4d22-a00c-6f3f098c8348)  
   ![image](https://github.com/user-attachments/assets/e298eaeb-f7f1-457f-90b5-6ed44fff81b8)

## 3. **Click Start, Write Your Bluetooth and Wi-Fi MAC Address and then Plug device to PC**  
   Ensure the addresses are similar but with different digits in the last two positions.  
   ![image](https://github.com/user-attachments/assets/3e30ab9f-058a-4a79-b38e-98fb241acd82)

## 4. **Unplug and Open mtkclient, Backup nvram**  
   ![image](https://github.com/user-attachments/assets/4c5a7601-9ae9-4c0a-a453-4d367fd557e2)

## 5. **Flash gpt_x04g.bin**  
   Run the command:  
   `python3 mtk.py wf gpt.bin --noreconnect`  
   ![image](https://github.com/user-attachments/assets/56cb3164-a6d8-4d74-a709-0b957f3a0bec)

## 6. **Flash All Dump_mico_x04g.tar.xz**  
   (If there’s an error, ignore it)  
   Run the command:  
   `python3 mtk.py wl --preloader preloader_mico_x04g.bin --noreconnect global`  
   ![image](https://github.com/user-attachments/assets/30a4b45a-0f31-4aaa-9b22-65f20963fc15)  
   ![image](https://github.com/user-attachments/assets/d15a0c81-d501-4904-a735-4c6300359304)

## 7. **Flash boot1_for_microx04g.bin to preloader in mtkclient GUI**  
   ![image](https://github.com/user-attachments/assets/22a25a20-4e75-4526-af3d-17f58907f0a7)
   ![image](https://github.com/user-attachments/assets/05bff5e2-27af-41dc-b083-dba256c97f0d)

## 8. **Restore nvram.bin from GongChengROM backup, and proinfo.bin from first backup in mtkclient**
   ![image](https://github.com/user-attachments/assets/a90ec6ea-4385-44fe-9e23-b1b02fc38c5d)
   ![image](https://github.com/user-attachments/assets/586400ad-fca3-4828-8916-521bcadb29e5)

## 9. **Replug to reboot and Enjoy!**
