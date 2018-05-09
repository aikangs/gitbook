# ubuntu18.04下安装Deepin Scrot
```base
wget http://packages.linuxdeepin.com/deepin/pool/main/d/deepin-scrot/deepin-scrot_2.0-0deepin_all.deb sudo dpkg -i deepin-scrot_2.0-0deepin_all.deb
```
如果安装后运行提示 ImportError: No module named gtk
这时候安装
```bash
sudo apt-get install python-gtk2
```
就可以了
