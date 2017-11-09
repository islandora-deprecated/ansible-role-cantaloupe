# Ansible Role: Cantaloupe

An Ansible role that installs [Cantaloupe](https://github.com/medusa-project/cantaloupe) in a Tomcat 8 servlet container on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

Version to install:
```
cantaloupe_version: 3.3.1
```

Where to install:
```
cantaloupe_install_root: /opt
```

Name of symlink to create:
```
cantaloupe_symlink: /opt/cantaloupe
```

Where to put log files:
```
cantaloupe_log_path: /var/log/cantaloupe
```

Cantaloupe user/group:
```
cantaloupe_user: cantaloupe
cantaloupe_group: cantaloupe
```

Whether to deploy the Cantaloupe war to the Tomcat webapps directory:
```
cantaloupe_deploy_war: no
```

Where to deploy wars to:
```
cantaloupe_deploy_war_path: /path/to/tomcat/webapps
```

What to name the war (which is also the Tomcat context path):
```
cantaloupe_deploy_war_filename: cantaloupe
```

There are many more options documented in the [defaults/main.yml](defaults/main.yml)

## Dependencies

* [islandora.tomcat8](https://github.com/Islandora-DevOps/ansible-role-tomcat8)
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.cantaloupe }

## License

MIT