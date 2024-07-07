# Custom plymouth-themes
Custom Plymouth themes for blackbeard distro which show a nice splash screen when booting up. Includes password prompt for encrypted drives as well.

# Installation
Dependencies should install along with plymouth. For more information on dependencies and plymouth visit:

https://archlinux.org/packages/extra/x86_64/plymouth/

```
sudo pacman -S plymouth cpio
```

Clone repo to /path/to/downloads
```
git clone git@github.com:cvusmo/plymouth-themes
cd plymouth-themes
```

plymouth-etc contains the plymouthd.conf which needs to be placed at /etc/

```
cd plymouth-etc
sudo mv plymouthd.conf /etc/
cd ..
```

plymouth-theme contains the theme for plymouth. This will need to be placed at /usr/share/

```
cd plymouth-theme
sudo mv plymouth /usr/share/
```

Next, update mkinitcpio.conf
```
sudo mkinitcpio.conf -P
```

Now reboot
```
sudo reboot
```
