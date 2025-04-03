# Convert Global Version to China Version

## Make Sure You Already Backup Your Partition

### `--noreconnect` is required for Windows, no need for Linux

## Tools:
1. [Download v2.99.99 firmware](https://xiaoai.qgmzmy.me/d/lx04/rom/%E5%AE%98%E6%94%B9/%E2%86%91%E5%B0%8F%E7%88%B1%E8%A7%A6%E5%B1%8F-LX04_2.99.99-%E5%AE%98%E6%94%B9-SP4%20(%E6%9C%80%E6%96%B0)%20.7z?sign=dCUpnRJHR1LeaykewEnzKdz750tAb_Lc9frDsoTogso=:0)
2. [SP Flash Tool](https://spflashtool.com/download/)
3. [Hikaru_resign-Xiaomi](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/Hikaru_resign-Xiaomi.7z)
4. [gpt_lx04.bin](https://github.com/AyraHikari/xiaomi-x04g-lx04/blob/main/files/gpt_lx04.bin)

# Guide:

## 1. **Flash gpt_x04g.bin**  
   Run the command:  
   `python3 mtk.py wf gpt.bin --noreconnect`  
   ![image](https://github.com/user-attachments/assets/56cb3164-a6d8-4d74-a709-0b957f3a0bec)

## 2. **Flash v2.99.99 firmware with FlashTool**  
   ![image](https://github.com/user-attachments/assets/9800ed60-7ccd-42ca-ab05-8ade2f6ca409)

## 3. Reboot
