# mysql-conf_centos
1.wget https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm 

2.yum localinstall mysql57-community-release-el7-11.noarch.rpm

3.yum repolist enabled | grep "mysql.*-community.*"

4.yum install mysql-community-server -y 

5.systemctl start mysqld

6.systemctl status mysqld

7.grep 'temporary password' /var/log/mysqld.log

8.mysql_secure_installation

9.mysql -u root -p 

for remote connection stop the firewall

10.systemctl stop firewalld

11.$EDITOR /etc/my.cnf

[mysqld]
bind-address = *

12.systemctl restart mysqld

13.mysql -u root -p

14.mysql> CREATE USER 'gmolica'@'%' IDENTIFIED BY 'Unixmen1!';

15.mysql> GRANT ALL PRIVILEGES ON *.* TO 'gmolica'@'%' IDENTIFIED BY 'Unixmen1!';

16.mysql> FLUSH PRIVILEGES;

17.mysql> EXIT;
