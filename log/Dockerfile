FROM  centos:latest
 
# Author of this Dockerfile
MAINTAINER Bala


 
# Update & upgrades
RUN yum install rsyslog -y

COPY rsyslog.conf /etc/rsyslog.conf
EXPOSE 514

RUN systemctl enable rsyslog

CMD  ["rsyslogd", "-dn"]
