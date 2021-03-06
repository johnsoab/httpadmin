Role Name
=========

This role sets up apache httpd to be managed by a group of users. It does not configure Apache HTTPD specifically.

Requirements
------------

This role sets up a group for webadmins, membership, file permissions to modify content in the webroot, read webserver log files,  as well as manage the httpd service and tls certificates

Role Variables
--------------

An array of users who should be webadmins is all that is necessary. These users will be added to the webadmin group, and granted rights to manage the httpd server.

Dependencies
------------

Role assumes RHEL/CentOS 7.x. Has not been checked against RHEL 6.x

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: httpadmin, sudoers: ["testuser1","testuser42"] }

License
-------

BSD

Author Information
------------------

andy.johnson@nielsen.com
