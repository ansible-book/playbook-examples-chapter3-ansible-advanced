---
#安装apache的play
- hosts: web
  remote_user: root
  tasks:
  - name: ensure apache is at the latest version
    yum: pkg=httpd state=latest

# 安装mysql server的play
- hosts: lb
  remote_user: root
  tasks:
  - name: ensure mysqld is at the latest version
    yum: pkg=mariadb state=latest
