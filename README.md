# 🎦 Xiaomi Camera Streamer


## Install / 安装

### Docker compose
```shell
mkdir /opt/micam
cd /opt/micam
wget https://raw.githubusercontent.com/miiot/micam/refs/heads/main/docker-compose.yml
docker compose up -d
```

> 此命令会通过docker部署Miloco、Go2rtc及RTSP转发服务。如果需要添加多个摄像头，需要编辑`docker-compose.yml`运行多个micam服务。
>
> 部署的Miloco为基础版，不带AI引擎，无GPU算力要求，大部分机器都能运行，但目前不支持arm架构。


## Usage / 使用

### [Miloco](https://github.com/XiaoMi/xiaomi-miloco)

> 你也可以选择通过[HAOS加载项](https://gitee.com/hasscc/addons)来部署Miloco，[一键添加](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgitee.com%2Fhasscc%2Faddons)加载项仓库。

1. Open Miloco WebUI / 打开Miloco网页: `https://192.168.1.xx:8000`
2. Set miloco password / 设置Miloco密码
3. Bind your Xiaomi account / 绑定小米账号
4. Camera offline ? [[Xiaomi Miloco Q&A]](https://github.com/XiaoMi/xiaomi-miloco/issues/56)


### [Go2rtc](https://github.com/AlexxIT/go2rtc)

> 你也可以选择通过[HAOS加载项](https://github.com/AlexxIT/hassio-addons)来部署Go2rtc

1. Open Go2rtc WebUI / 访问Go2rtc网页: `http://192.168.1.xx:1984`
2. Config empty streams / 配置空视频流:
   ```yaml
   streams:
      your_stream1:
      your_stream2:
   ```
3. Save & Restart


### Micam

1. Set environment variables / 设置环境变量:
   ```shell
   cat << EOF > .env
   MILOCO_PASSWORD=your_miloco_password_md5
   CAMERA_ID=1234567890 # your camera did
   RTSP_URL=rtsp://go2rtc:8554/your_stream1
   EOF
   ```
2. Restart micam / 重启转发服务: `docker compose restart micam1`
