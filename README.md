## Mosquitto Server (MQTT)

Ports Exposed

```
EXPOSE 1883
EXPOSE 8883
EXPOSE 9883
```


Notes:
- To Patch Libressl `libressl.patch`
- docker long running process `run.sh`
- Mosquitto Configuration File `mosquitto.conf` which would be mounted on `/etc/mosquitto/mosquitto.conf`
- Auth Plugin `auth-plugin.conf` which is going to be located at this location `/var/lib/mosquitto/`



```
docker run -it -p 1883:1883 -p 9001:9001 -v ./mosquitto.conf:/etc/mosquitto/mosquitto.conf vishwassharma/mqtt-auth:1.4.14
```