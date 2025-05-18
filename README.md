# Overview

This repo has fixes for the Win 2 + Bazzite and ChimeraOS. This uses nbfc for fan controls.

# Note:
 - nbfc requires secure boot to be disabled at BIOS, if you need to reboot directly to BIOS you can run
`sudo systemctl reboot --firmware-setup`

# Bazzite instructions

Bazzite doesn't need custom gamescope, tested in Bazzite v41 on a GPD Win 2 m3-7y30. However, nbfc does need to be manually installed for fan controls.

You may encounter a bug where the screen is blank/black during the install process. Workaround is to plug in an external monitor while booting the installer, display via usb-c adapter should work fine too.

```bash
# installs nbfc
curl -L https://github.com/aarron-lee/bazzite-win2/raw/main/bazzite_fix.sh | sh
```

You can use [SimpleDeckyTDP](https://github.com/aarron-lee/SimpleDeckyTDP) for EPP and power governor controls, unfortunately TDP controls currently don't work. You can disable TDP controls in SDTDP's settings.

You can also use [steam-powerbuttond](https://github.com/ShadowBlip/steam-powerbuttond) for to get the power button to sleep the device.

```bash
curl -L https://github.com/ShadowBlip/steam-powerbuttond/raw/main/bazzite_install.sh | sh
```
