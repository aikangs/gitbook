# ubuntu下golang的交叉编译

先安装go1.4.2

```bash
wget https://storage.googleapis.com/golang/go1.4.2.linux-amd64.tar.gz
```

设置环境变量
```bash
 GOROOT_BOOTSTRAP=/home/aikangs/app/go1.4.2
 export GOROOT_BOOTSTRAP
 export PATH=${PATH}:${GOROOT_BOOTSTRAP}
```

最后进入GOROOT/src目录运行你需要编译的平台的代码

```bash
# 如果你想在Windows 32位系统下运行
  ~$CGO_ENABLED=0 GOOS=windows GOARCH=386 ./make.bash

# 如果你想在Windows 64位系统下运行
  ~$CGO_ENABLED=0 GOOS=windows GOARCH=amd64 ./make.

# 如果你想在OS X 32位系统下运行
  ~$CGO_ENABLED=0 GOOS=darwin GOARCH=386 ./make.bash

# 如果你想在OS X 64位系统下运行
  ~$CGO_ENABLED=0 GOOS=darwin GOARCH=amd64 ./make.bash

# 如果你想在Linux 32位系统下运行
  ~$CGO_ENABLED=0 GOOS=linux GOARCH=386 ./make.bash

# 如果你想在Linux 64位系统下运行
  ~$CGO_ENABLED=0 GOOS=linux GOARCH=amd64 ./make.bash
```
最后编译时，进入你的项目目录
运行

```bash
# 如果你想在Windows 32位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=windows GOARCH=386 go build main.go

# 如果你想在Windows 64位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build main.go

# 如果你想在OS X 32位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=darwin GOARCH=386 go build main.go

# 如果你想在OS X 64位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=darwin GOARCH=amd64 go build main.go

# 如果你想在Linux 32位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=linux GOARCH=386 go build main.go

# 如果你想在Linux 64位系统下运行
➜  ~$CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build main.go
```





