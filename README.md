# MQTT for Docker(HASS)

��������һ�����õı��� Docker ��װ�� MQTT ������������������ `mosquitto`����Ҫ���ݲ��� [ncarlier/mqtt](https://hub.docker.com/r/ncarlier/mqtt)�����Ǽ�����Ҫ��Ϊ�˸�HASS�������豸�ṩ�������ã�����������һЩ��ص�����

# ���ӵ���������

������ /etc/mosquitto/mosquitto.conf �ļ�����������������

```
port 1883
listener 1884
protocol websockets
allow_anonymous false
```

# ʹ�÷���

��������þ�������Docker���ɣ�Ȼ��ͨ������̨�����������������û�������

```
mosquitto_passwd -b /etc/mosquitto/pwfile.example username password
```

������Ȼ�����������������ʱ��ֱ��ʹ��CMD����������Ҳ�ǿ��Եġ�