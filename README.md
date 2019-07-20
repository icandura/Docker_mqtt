# MQTT for Docker(HASS)

　　这是一个家用的便于 Docker 安装的 MQTT 服务器，服务器采用 `mosquitto`。主要内容参照 [ncarlier/mqtt](https://hub.docker.com/r/ncarlier/mqtt)。但是家里主要是为了给HASS下属的设备提供服务器用，所以增加了一些相关的配置

# 增加的配置内容

　　在 /etc/mosquitto/mosquitto.conf 文件中增加了以下内容

```
port 1883
listener 1884
protocol websockets
allow_anonymous false
```

# 使用方法

　　加入该镜像启动Docker即可，然后通过控制台采用以下命令设置用户名密码

```
mosquitto_passwd -b /etc/mosquitto/pwfile.example username password
```

　　当然如果想在运行容器的时候直接使用CMD命令来运行也是可以的。