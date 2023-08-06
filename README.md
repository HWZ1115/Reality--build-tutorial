# **installation**
### Install the sing-box program
- **Debian && Ubuntu**
- ***AMD***
```
apt -y update && apt -y install wget && wget -c "https://github.com/SagerNet/sing-box/releases/download/v1.3.0/sing-box-1.3.0-linux-amd64.tar.gz" -O - | tar -xz -C /usr/local/bin --strip-components=1 && chmod +x /usr/local/bin/sing-box
```
- ***ARM***
```
apt -y update && apt -y install wget && wget -c "https://github.com/SagerNet/sing-box/releases/download/v1.3.0/sing-box-1.3.0-linux-arm64.tar.gz" -O - | tar -xz -C /usr/local/bin --strip-components=1 && chmod +x /usr/local/bin/sing-box
```
- **CentOS**
- ***AMD***
```
yum update && yum -y install wget && wget -c "https://github.com/SagerNet/sing-box/releases/download/v1.3.0/sing-box-1.3.0-linux-amd64.tar.gz" -O - | tar -xz -C /usr/local/bin --strip-components=1 && chmod +x /usr/local/bin/sing-box
```
- ***ARM***
```
yum update && yum -y install wget && wget -c "https://github.com/SagerNet/sing-box/releases/download/v1.3.0/sing-box-1.3.0-linux-arm64.tar.gz" -O - | tar -xz -C /usr/local/bin --strip-components=1 && chmod +x /usr/local/bin/sing-box
```
### Configure the systemd service of sing-box
```
wget -P /etc/systemd/system https://raw.githubusercontent.com/TinrLin/Reality--build-tutorial/main/sing-box.service
```
### Download and modify the sing-box configuration file
- **Vless+vision+Reality**
```
mkdir -p /usr/local/etc/sing-box/ && wget -O /usr/local/etc/sing-box/config.json https://raw.githubusercontent.com/TinrLin/Reality--build-tutorial/main/vless_vision_reality_config.json
```
- **Vless+h2+Reality**
```
mkdir -p /usr/local/etc/sing-box/ && wget -O /usr/local/etc/sing-box/config.json https://raw.githubusercontent.com/TinrLin/Reality--build-tutorial/main/vless_h2_reality_config.json
```
- **Vless+gRPC+Reality**
```
mkdir -p /usr/local/etc/sing-box/ && wget -O /usr/local/etc/sing-box/config.json https://raw.githubusercontent.com/TinrLin/Reality--build-tutorial/main/vless_grpc_reality_config.json
```
### Start and run sing-box
```
systemctl daemon-reload && systemctl enable --now sing-box && systemctl status sing-box
```
