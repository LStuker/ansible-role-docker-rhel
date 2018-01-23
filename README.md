Docker
=========

An Ansible Role that installs [Docker](https://www.docker.com) on RHEL/Centos 7 system.

- Add repository https://download.docker.com/linux/centos/docker-ce.repo
- Activate stable repo
- Install docker-ce
- Install python-docker-py


Requirements
------------

RHEL/Centos 7 system

Role Variables
--------------

# Edition can be one of: 'ce' (Community Edition) or 'ee' (Enterprise Edition).

```
docker_edition: 'ce'
docker_package: "docker-{{ docker_edition }}"
docker_package_state: present
```

# Used only for RedHat/CentOS.
```
docker_yum_repo_url: https://download.docker.com/linux/centos/docker-{{ docker_edition }}.repo
docker_yum_release_channel: stable
```

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: servers
      roles:
         - docker

License
-------

MIT

Author Information
------------------

This role was created by [Lucien Stuker](https://www.newbit.ch/)
inspired by: https://github.com/geerlingguy/ansible-role-docker
