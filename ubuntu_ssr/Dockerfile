FROM ubuntu
RUN apt-get update && apt-get install -y wget
COPY ss-fly/ss-fly /bin/ss-fly
COPY ss-fly/ss-fly.sh /bin/ss-fly.sh
COPY ss-fly/sshelp /bin/sshelp
COPY ss-fly/v2ray.sh /bin/v2ray.sh
EXPOSE 2333
WORKDIR /bin
RUN ss-fly.sh -i 12345687 2333 && ss-fly.sh -bbr
ENTRYPOINT ssserver -c /etc/shadowsocks.json -d start && /bin/bash
