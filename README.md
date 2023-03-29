# Penguin theme for Plymouth

### Thanks to [EREN16](https://www.gnome-look.org/p/1805336) who prepared this theme.

## Installation

Let's clone the repo and enter the folder:
```bash
git clone https://github.com/yucellmustafa/plymouth-linux /tmp/plymouth-linux && /tmp/plymouth-linux
```

Copy the selected theme in plymouth theme dir:
```bash
sudo cp -r linux-penguin /usr/share/plymouth/themes/
```

### for Fedora:
```bash
# check if theme exist in dir
sudo plymouth-set-default-theme -l

# now set the theme (linux-penguin, in this case) and rebuilt the initrd
sudo plymouth-set-default-theme -R linux-penguin
```

### for Ubuntu:
```bash
# install the new theme (linux-penguin, in this case)
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/angular/linux-penguin.plymouth 100

# select the theme to apply
sudo update-alternatives --config default.plymouth
#(select the number for installed theme, angular in this case)

# update initramfs
sudo update-initramfs -u
```

![image](https://user-images.githubusercontent.com/49123562/228576333-24c6e63a-8c35-4892-9212-aae21e4c18bf.png)
