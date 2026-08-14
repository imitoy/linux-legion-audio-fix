# linux-legion-audio-fix
Arch Linux pacman repository: Legion laptop audio fix packages (linux kernel + aw88399 ACF firmware)

Patches url: https://github.com/nadimkobeissi/16iax10h-linux-sound-saga

# Instructions
1. Add this repository by editing `/etc/pacman.conf`:

```conf
[linux-legion-audio-fix]
SigLevel = Optional
Server = https://imitoy.github.io/linux-legion-audio-fix
```

2. Install pre-build packages.
```bash
sudo pacman -Syu linux-legion-audio-fix aw88399-acf-firmware
```

3. Update grub config
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

4. Reboot.
```bash
sudo reboot
```
5. Choose linux-legion-audio-fix kernel in your grub menu.
