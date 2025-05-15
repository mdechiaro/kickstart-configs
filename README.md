Add kickstart files to ISOs

1. Download ISO from vendor
2. Use `xorriso` to add ks.cfg and grub.cfg to ISO

```
xorriso -indev /path/to/original.iso \
   -outdev /path/to/new.iso \
   -volid "FEDORA" \
   -add ks.cfg -- \
   -pathspecs on -add boot/grub2/grub.cfg grub.cfg -- \
   -boot_image any replay --
```

3. Boot the ISO
