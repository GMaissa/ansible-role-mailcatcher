Mailcatcher
========
[![Travis branch](https://img.shields.io/travis/GMaissa/ansible-role-mailcatcher/master.svg)](https://travis-ci.org/GMaissa/ansible-role-mailcatcher)
[![Galaxy](http://img.shields.io/badge/galaxy-GMaissa.mailcatcher-blue.svg?style=flat)](https://galaxy.ansible.com/list#/roles/3686)

This Ansible Mailcatcher role is a fork of [Stephan Hochhaus' one](https://github.com/yauh/role-mailcatcher), in order to add support for RHEL / Centos.

It installs [Mailcatcher](http://mailcatcher.me) on your system and starts it upon boot time.

Requirements
------------

No external requirements exist to this role.

Role Variables
--------------

    mailcatcher_ip: 0.0.0.0       # Set the ip address of both servers
    mailcatcher_smtp_ip: 0.0.0.0  # Set the ip address of the smtp server
    mailcatcher_smtp_port: 1025   # Set the ip address of the smtp server
    mailcatcher_http_ip: 0.0.0.0  # Set the ip address of the http server
    mailcatcher_http_port: 1080   # Set the port address of the http server


License
-------

BSD

Author Information
------------------

Guillaume Maïssa <pro.g@maissa.fr>
