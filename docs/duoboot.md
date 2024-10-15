## Fix windows update overwriting /efi/boot
- Load the efi partion

```bash
sudo mount /dev/sda1 /mnt/efi
```

The folder structure will probably be line
```
/mnt/efi/EFI/
├── Boot/
│   └── bootx64.efi
├── Microsoft/
│   ├── Boot/
│   │   ├── bootmgfw.efi
│   │   ├── BCD
│   │   ├── memtest.efi
│   │   └── other boot-related files
```

rename the `bootmgfw.efi` to `ori_bootmgfw.efi`. Copy `grub.efi` to the directory and rename it as the original windows efi, `bootmgfw.efi`. Reboot the PC should boot into grub
