# Fix broken partition
If mtkclient GUI return None and you can't flash anything, this can be fixed
## `--noreconnect` is required for windows, no need for linux

1. Flash global ROM with global preloader
`python3 mtk.py wl --preloader preloader_mico_x04g.bin --noreconnect global`
