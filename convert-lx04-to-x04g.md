# Convert China version to Global version

## Make sure you already backup your partition

### `--noreconnect` is required for windows, no need for linux

1. Flash GongChengROM with FlashTool

If you booted it on latest batch, it will glitches.
Don't worry it wont broken, it just missing driver and we don't need it for rewrite MAC.

2. Unplug device, open SN_Write_Tool and set to same to picture

3. Click start and write your Bluetooth and WIFI MAC address (make it similar but with different digit on last two address)

4. Unplug and open mtkclient, backup nvram

8. Flash gpt.bin from dump_mico_x04g.tar.xz
`python3 mtk.py wf gpt.bin --noreconnect`

9. Flash all dump_mico_x04g.tar.xz
`python3 mtk.py wl --preloader preloader_mico_x04g.bin --noreconnect global`

10. Flash boot1_for_microx04g.bin in mtkclient GUI

11. Restore nvram.bin in mtkclient

12. Reboot and enjoy
