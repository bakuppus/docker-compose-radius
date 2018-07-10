#  Docker compose #
###################

# To run compose

1. git clone https://github.com/bakuppus/docker-compose-radius.git

2. docker-compose up -d

#Result 

[root@ip-172-31-84-17 Project1]# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                                                                                  NAMES
a5cbeee7fc62        project1_log        "rsyslogd -dn"           9 minutes ago       Up 9 minutes        0.0.0.0:514->514/tcp                                                                   project1_log_1
522a94247672        project1_db         "/docker-entrypoin..."   9 minutes ago       Up 9 minutes        0.0.0.0:3307->3306/tcp                                                                 project1_db_1
11fde90ffe44        project1_ssh        "/usr/sbin/sshd -D"      9 minutes ago       Up 9 minutes        0.0.0.0:2222->22/tcp                                                                   project1_ssh_1
2f6bb4ae2906        project1_radius     "radiusd -xx -f"         9 minutes ago       Up 9 minutes        1812-1813/udp, 0.0.0.0:1812-1813->1812-1813/tcp, 18120/udp, 0.0.0.0:18120->18120/tcp   project1_radius_1
84d645ffec18        project1_web        "/usr/sbin/httpd -..."   9 minutes ago       Up 9 minutes        0.0.0.0:80->80/tcp                                                                     project1_web_1
[root@ip-172-31-84-17 Project1]#




############################  
# please report issue  here
https://github.com/bakuppus/docker-compose-radius/issues
###########################
