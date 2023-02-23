# x79btc-modified-bios
modified uefi bios to enable all cores on chinese x79btc, btc79x5, x79eth03 motherboards.

from the factory these boards have all cpus locked to 2 cores to reduce heat+power when gpu mining.

you may want to use a larger cpu heatsink after enabling all cores.

bios can be flashed with flashrom:
```bash
sudo flashrom -w modded.rom -p internal -c MX25L6436E/MX25L6445E/MX25L6465E/MX25L6473E/MX25L6473F
```

also included is original bios rom as dumped from flashrom:
```bash
sudo flashrom -p internal -c MX25L6436E/MX25L6445E/MX25L6465E/MX25L6473E/MX25L6473F -r original.rom
```
