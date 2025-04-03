# Convert China version to Global version

## Make sure you already backup your partition

### `--noreconnect` is required for windows, no need for linux

## Tools:
1. [Download GongChengROM](https://xiaoai.qgmzmy.me/d/lx04/rom/%E5%B7%A5%E7%A8%8Brom/GongChengROM.zip?sign=XUYpVHg_ulRWQxfyrwZo-RZP0H-T70XXk7jV9n3OkHA=:0)
2. [SP Flash Tool](https://spflashtool.com/download/)
3. [Hikaru_resign-Xiaomi](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/Hikaru_resign-Xiaomi.7z)

## Guide:
1. Flash GongChengROM with FlashTool
![image](https://github.com/user-attachments/assets/870fe5e8-da0a-43ce-b372-e8645a4f824e)

If you booted it on latest batch, it will glitches.
Don't worry it wont broken, it just missing driver and we don't need display driver for rewrite MAC.
![image](https://github.com/user-attachments/assets/4730eb94-54ba-4236-bef7-24e65e36323b)

2. Unplug device, open SN_Write_Tool and set to same to picture
![image](https://github.com/user-attachments/assets/b644ffb7-0f60-4d22-a00c-6f3f098c8348)
![image](https://github.com/user-attachments/assets/e298eaeb-f7f1-457f-90b5-6ed44fff81b8)

3. Click start and write your Bluetooth and WIFI MAC address (make it similar but with different digit on last two address)
![image](https://github.com/user-attachments/assets/3e30ab9f-058a-4a79-b38e-98fb241acd82)

4. Unplug and open mtkclient, backup nvram
![image](https://github.com/user-attachments/assets/4c5a7601-9ae9-4c0a-a453-4d367fd557e2)

5. Flash gpt.bin from dump_mico_x04g.tar.xz
`python3 mtk.py wf gpt.bin --noreconnect`
![image](https://github.com/user-attachments/assets/56cb3164-a6d8-4d74-a709-0b957f3a0bec)

6. Flash all dump_mico_x04g.tar.xz (if there's an error, ignore it)
`python3 mtk.py wl --preloader preloader_mico_x04g.bin --noreconnect global`
![image](https://github.com/user-attachments/assets/30a4b45a-0f31-4aaa-9b22-65f20963fc15)
![image](https://github.com/user-attachments/assets/d15a0c81-d501-4904-a735-4c6300359304)

7. Flash boot1_for_microx04g.bin in mtkclient GUI
![image](https://github.com/user-attachments/assets/0ece596a-861f-440e-9529-13f7a5a9eb9c)
![image](https://github.com/user-attachments/assets/05bff5e2-27af-41dc-b083-dba256c97f0d)

8. Restore nvram.bin in mtkclient

9. Reboot and enjoy
