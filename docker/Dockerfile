FROM ubuntu:19.04 as base

RUN apt-get update && \
    apt-get install wget unzip openjdk-8-jdk-headless -y
RUN mkdir /opt/verapdf
WORKDIR /opt/verapdf
RUN wget http://downloads.verapdf.org/rel/verapdf-installer.zip && unzip verapdf-installer.zip && chmod +x verapdf-greenfield-1.14.8/verapdf-install
COPY auto-install.xml /opt/verapdf/verapdf-greenfield-1.14.8/
RUN ls -l ./verapdf-greenfield-1.14.8/ && ./verapdf-greenfield-1.14.8/verapdf-install auto-install.xml
