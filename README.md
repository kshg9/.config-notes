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
setup `mpv` and `ffmpeg` after setting up rpmfusion's repo.

Otherwise:
The `--allowerasing` flag is exactly what you need here — it will replace `ffmpeg-free` with RPM Fusion's full `ffmpeg`:

```bash
sudo dnf install ffmpeg --allowerasing
```

This will remove the Fedora-provided `ffmpeg-free` package and replace it with RPM Fusion's version, which includes all the proprietary codecs (libx264, libx265, AAC, etc.).
Has much better speed!

Printer-configs
```bash
https://github.com/ValdikSS/captdriver
```

Gnome tiling window manager extra setting. "Pop-Shell"
```bash
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-1 "['<Super>1']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-2 "['<Super>2']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-3 "['<Super>3']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-4 "['<Super>4']"
```
determinate-nix setup.

application list:
starship
ghidra
mise {java, node, etc}

imhex
radare2
ghidra

jetbrains-toolbox {androidstudio etc setup)
discord+vencord

vicinae
helium (browser)
kitty
sioyek
telegram
kitty
zed
obsidian
zeal {c++ plugin}
