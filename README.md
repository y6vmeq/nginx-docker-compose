nginx-docker-compose role
=========

## Summary

This Ansible role has the following features for:

**OpenJDK**

- Install docker
- Install docker-compose
- Deploy docker-compose projects


## Role Variables
# Docker  options
  - `docker_install` 
    - `true` (default)
    - `false`
  - `docker_edition: 'ce'`
    - `'ce'` (default)
    - `ee`
  - `docker_version`
    - `18.06` (default)

# Docker Compose options
  - `docker_install_compose`
    - `true` (default)
    - `false`
  - `docker_compose_version`
    - `latest` (default)
  
# Deploy options
  - `deploy_compose`
    - `true` (default)
    - `false`
  - `deploy_projects`
    - `nginx`

# For Python 3, use python3-pip.
  - `pip_install: true`
    - `true` (default)
    - `false`
  - `pip_package`
    - `python3` (default)
    - `python`
  - `pip_install_packages:`
    - `pip`
    - `setuptools`
    - `PyYAML`
    - `docker`

Example Playbook
----------------
### Deploy reverse proxy nginx:
```yaml
- name: Deploy reverse proxy nginx
  hosts: all
  become: true
  roles:
    - nginx-docker-compose
```

Author Information
------------------

authors:
  - Aliaksandr Padrabinkin <y6vmeq@gmail.com>
