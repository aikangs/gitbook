# linux 下修改virtualBox的动态磁盘大小

## 1:获取要修改的UUID
```bash
vboxmanage list hdds
UUID: 79d65850-6846-40c3-a8e7-715b199d1673
```
## 2:使用以下命令直接修改;
```bash
vboxmanage modifyhd 422d3782-4818-47d7-8d03-0e86325572a0 –resize $((40*1024)) 40*1024 表示重新指定大小到 40G
```