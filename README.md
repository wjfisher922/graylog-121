# Overview

This is a mix of [graylog2 open-core](https://github.com/Graylog2/docker-compose/blob/main/open-core/docker-compose.yml) and [graylog2 docker install docs.](https://go2docs.graylog.org/5-0/downloading_and_installing_graylog/docker_installation.htm)

# Usage

```
docker compose up
```

Access graylog [here.](http://localhost:9000)

nxlog.conf is the Window NXLOG configuration for sending GELF format logs to Graylog. Replace the default C:\Program Files\nxlog\conf\nxlog.conf with the one https://raw.githubusercontent.com/lawrencesystems/graylog/master/nxlog.conf and change the IP address to match your Graylog server.

# Install Instructions

1. Install Ubuntu Server Vm
2. Install Upadate: ```udo apt update && sudo apt upgrade -y```
3. Set timezone: ```sudo timedatectl set-timezone UTC```
4. Install git: ```sudo apt-get install git```
5. Clone repository: ```git clone https://github.com/lawrencesystems/graylog.git```
6. Install Docker: ```sudo apt-get install docker-compose```
7. Add local user to docker: ```sudo usermod -aG docker $USER```
8. Create a password to use for admin in docker-compose.xml: ```echo -n YourPassword | shasum -a 256```


# Extractors
UniFi: https://github.com/lawrencesystems/graylog_extractors
SonicWall: https://github.com/eduardohki/graylog-content-pack-sonicwall
