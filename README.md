## ⚙️ fedora notes.

Minimal Notes & sources to get by setting up.

setup on lenovo ideapad gaming 3
setup `tlp` `tlp-rdw` `lm_sensors`
setup nvidia drivers from rpmfusion

## rpmfusion's HowTO
 setup working nvidia card.
 setup the modeset.
 setup the videos lag issues.
 `sudo dnf install libva-nvidia-driver`

 
```bash
# cat /etc/default/grub
GRUB_CMDLINE_LINUX="rhgb quiet rd.driver.blacklist=nouveau,nova_core modprobe.blacklist=nouveau,nova_core nvidia-drm.modeset=1 nvidia.NVreg_PreserveVideoMemoryAllocations=1"
```

setup the grub commandline and vmlinuz image
```bash
sudo dracut -f
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
```
