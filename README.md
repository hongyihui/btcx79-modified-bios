# x79btc-modified-bios
modified uefi bios to enable all cores on chinese x79btc, btc79x5, x79eth03 motherboards. Also enables intel turbo boost. I don't have access to the btc79x9 dual-cpu variant so I don't recommend flashing that board.

from the factory these boards have all cpus locked to 2 cores to reduce heat+power when gpu mining.

you may want to use a larger cpu heatsink after enabling all cores.

bios can be flashed with flashrom:
```bash
sudo flashrom -w modded.rom -p internal -c MX25L6436E/MX25L6445E/MX25L6465E/MX25L6473E/MX25L6473F
```

also included is original bios rom as dumped from flashrom (bios v4.6.5 build date: 05/06/2021):
```bash
sudo flashrom -p internal -c MX25L6436E/MX25L6445E/MX25L6465E/MX25L6473E/MX25L6473F -r original.rom
```

flash chip is MX25L6436F labeled KH25L6436F

flash at your own risk. recommended to first dump your original rom and have a ch341a or other flash programmer available to recover in case of bad flash

![bios screenshot]("screenshot.png) ![htop screenshot]("htop.png)
