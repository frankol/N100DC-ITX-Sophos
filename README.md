# N100DC-ITX-Sophos-
a way to get Sophos Home running on a Asrock N100DC-ITX

Boot with prepared UEFI USB Stick
```
 fs0:
 cd EFI
 cd BOOT
 Bootx64.efi
 cd ..
 cd ..
 Fpt.efi -F MOD1-N100DC-ITX_2.01.ROM -BIOS
 reboot

```

Now you will see 2x Advanced in your BIOS after pressing F6. There you can activate CSM, but remember to select UEFI only for Video Card or you wont get a image anymore
I have attached my saved bios settings in "sophos-settings-uefi.BIN". You can restore it in your BIOS to get Sophos running

You wont see any output after BIOS start, so you need a serial converter attached to sub-d connector (baud rate 38400)

```
MOD1-N100DC-ITX_2.01.ROM = swapped Tools with hidden Advanced Menu
MOD2-N100DC-ITX_2.01.ROM = swapped Tools with hidden Advanced Menu + Swapped OC settings with hidden PCH-IO Menu to be able disable HPET (but not needed for sophos)

```
I tried million of combinations in bios to get sophos running, but i dont know which one extactly it was, so i made a UEFI Backup of all settings which you can restore
If something goes wrong you can flash the original bios i have attached too
