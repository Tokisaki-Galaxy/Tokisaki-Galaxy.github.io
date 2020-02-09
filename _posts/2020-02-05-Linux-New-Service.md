---
layout: post
title: Linux新建服务
date: 2020-02-05
tag: Linux
---

```
sudo nano /lib/systemd/system/xxx.service
```

```
[Unit]
Description=Your Service Name
After=network.target syslog.target
Wants=network.target

[Service]
Type=simple
ExecStart=Your File Path

[Install]
WantedBy=multi-user.target
```

```
systemctl daemon-reload
systemctl start frpc.service
```
