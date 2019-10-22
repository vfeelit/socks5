# SOCKS5 - 基于PHP WorkerMan框架，实现SOCKS5协议

## 克隆项目并安装依赖
```bash
#下载
git clone https://github.com/vfeelit/socks5.git
#进入目录
cd socks5

#安装依赖
composer -vvv install
```

## 定义环境变量
拷贝根目录下的.env.example，重命名为.env:
```bash
DAEMONIZE=true
NAME=SS5
LISTEN=tcp://0.0.0.0:21080
WORKER_COUNT=16
MAX_REQUEST=8000
STDOUT=
PID_FILE=
LOG_FILE=
STATISTICS_FILE=
WORKER_USER=
WORKER_GROUP=
#MAX_PACKAGE_SIZE=
#MAX_SEND_BUFFER_SIZE=
SOCKET_BACKLOG=102400
SOCKET_RECV_TIMEOUT=60
SOCKET_SND_TIMEOUT=60
```
LISTEN控制监听地址，WORKER_COUNT控制Worker进程数量。

## 运行项目
```bash
#运行
php bin/ss start

#停止
php bin/ss stop

#重新加载
php bin/ss reload

#查看状态
php bin/ss status
```



