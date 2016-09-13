FROM ubuntu:14.04 

ADD sources.list_aliyun /etc/apt/sources.list
RUN sudo apt-get update;
RUN sudo apt-get -dy --reinstall install libc6-i386
RUN sudo apt-get install -y lib32z1 lib32ncurses5 lib32bz2-1.0 wget
RUN wget --ftp-user=upload --ftp-password="{;9ZR#V}27bWIC3" ftp://182.92.72.171/software/aksusbd-7.40.1-i386.tar
RUN tar -xvf aksusbd-7.40.1-i386.tar
RUN cd aksusbd-7.40.1-i386 && sudo ./dinst