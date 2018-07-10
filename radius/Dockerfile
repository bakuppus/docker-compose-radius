FROM  centos:latest
MAINTAINER Bala

RUN yum install wget epel-release rsyslog openssh-server openssh-clients gnutls freetds freetds-devel cpanm gcc perl perl-App-cpanminus perl-Config-Tiny freeradius freeradius-utils freeradius-mysql freeradius-perl unixODBC unixODBC-devel -y
RUN export SYBASE=/usr
RUN cpanm install Crypt::OpenSSL::AES Crypt::CBC Digest::SHA Digest::SHA1 Params::Validate Digest::MD5 Rest::Client DBI DBD::ODBC DBD::Sybase JSON  LWP REST::Client Net::Syslog YAML List:MoreUtils  &


user root
# Datetime.pm
RUN usermod -p "!" root

EXPOSE 1812/udp 1813/udp 18120/udp

# Run FreeRADIUS
RUN chown -R radiusd.radiusd /var/run/radiusd /var/log/radius



USER root

CMD ["radiusd","-xx","-f"]
