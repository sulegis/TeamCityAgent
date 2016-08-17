FROM registry.cn-hangzhou.aliyuncs.com/cubic/ciagent-ubuntu16-jdk8-mvn:latest

ENV UGO_HOME  /opt/UGO
ENV PATH $UGO_HOME/Bin:$PATH
ENV LD_LIBRARY_PATH $UGO_HOME/Bin:$LD_LIBRARY_PATH

RUN cd /tmp && wget -O SMO.tar.gz ftp://ftp.ispeco.com/ugo/Linux64/SMO_Java_810_14004_57241_64_x64_linux_gcc_Bin.tar.gz \
	&& mkdir -p $UGO_HOME && tar -zxvf /tmp/SMO.tar.gz -C $UGO_HOME

RUN cd /tmp && wget -O aksusbd.tar ftp://ftp.ispeco.com/PackageSrc/aksusbd_2.4.1-i386.tar \
	&& tar -xvf aksusbd.tar && mv ./aksusbd-* /opt/aksusbd
