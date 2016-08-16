FROM ubuntu:16.04 

ENV AGENT_DIR  /opt/buildAgent

#supermap libs
RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
		lxc iptables aufs-tools ca-certificates curl wget unzip software-properties-common language-pack-en \
	&& apt-get install -y libx11-dev xinit gcc libgomp1 libxtst6 libxi6 libc6-i386 language-pack-zh-hans \
	&& rm -rf /var/lib/apt/lists/*

ENV LANG zh_CN.UTF-8
ENV LC_CTYPE zh_CN.UTF-8

#entrypoint
ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]

VOLUME /opt/buildAgent

EXPOSE 9090

