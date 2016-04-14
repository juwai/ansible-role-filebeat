Ansible Role: Filebeat
=========

Install Filebeat on CentOS servers.

Requirements
------------

Written in Ansible 1.9.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### supervisord_config_dir

Directory where supervisord reads configuration files.

Default is `/etc/supervisor.d`.

### filebeat_supervisor_enabled

Install filebeat in supervisor or not.

Default is true.

### filebeat_version

Filebeat version.

Default is `1.0.1`.

### filebeat_rpm_url

URL where to download filebeat.

Default is `https://download.elastic.co/beats/filebeat/filebeat-1.0.1-x86_64.rpm`.

### filebeat_config_dir

Directory for filebeat configuration file.

Default is `/etc/filebeat`.

### filebeat_log_dir

Directory for filebeat log files.

Default is `/var/log/filebeat`.

### filebeat_group

Group for filebeat user.

Default is `filebeat`.

### filebeat_user

Filebeat user.

Default is `filebeat`.

### filebeat_config

Filebeat configuration. Contents are copied as YAML directly to configuration file.

Dependencies
------------

+ juwai.supervisor, when filebeat_supervisor_enabled

Example Playbook
----------------

    - hosts: servers
      roles:
         - juwai.filebeat

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2016 by [Juwai Limited](http://www.juwai.com).
