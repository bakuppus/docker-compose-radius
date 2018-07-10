#  Docker compose #
###################

# To run compose

1. git clone https://github.com/bakuppus/docker-compose-radius.git

2. docker-compose up -d

#Result 

docker-compose ps

      Name                     Command               State                                                    Ports
---------------------------------------------------------------------------------------------------------------------------------
project1_db_1       /docker-entrypoint.sh mysq ...   Up      0.0.0.0:3307->3306/tcp
project1_log_1      rsyslogd -dn                     Up      0.0.0.0:514->514/tcp
project1_radius_1   radiusd -xx -f                   Up      0.0.0.0:1812->1812/tcp, 1812/udp, 0.0.0.0:18120->18120/tcp, 18120/udp, 0.0.0.0:1813->1813/tcp, 1813/udp
project1_ssh_1      /usr/sbin/sshd -D                Up      0.0.0.0:2222->22/tcp
project1_web_1      /usr/sbin/httpd -D FOREGROUND    Up      0.0.0.0:80->80/tcp


############################  
# please report issue  here
https://github.com/bakuppus/docker-compose-radius/issues
###########################
