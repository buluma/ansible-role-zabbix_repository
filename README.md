# [Ansible role zabbix_repository](#zabbix_repository)

Install and configure zabbix_repository on your system.

|GitHub|GitLab|Downloads|Version|Issues|Pull Requests|
|------|------|-------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-zabbix_repository/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-zabbix_repository/actions)|[![gitlab](https://gitlab.com/shadowwalker/ansible-role-zabbix_repository/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-zabbix_repository)|[![downloads](https://img.shields.io/ansible/role/d/4888)](https://galaxy.ansible.com/buluma/zabbix_repository)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.zabbix_repository
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: buluma.bootstrap
    - role: buluma.ca_certificates
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/defaults/main.yml):

```yaml
---
# defaults file for zabbix_repository

# The`"zabbix_version_major` are two numerical values, sparated by a period.
zabbix_repository_version_major: "5.4"

# The `zabbix_version_minor` is a single numerical value.
zabbix_repository_version_minor: 1
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.ca_certificates](https://galaxy.ansible.com/buluma/ca_certificates)|[![Build Status GitHub](https://github.com/buluma/ansible-role-ca_certificates/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-ca_certificates/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-ca_certificates/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-ca_certificates)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-zabbix_repository/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|bullseye|
|[opensuse](https://hub.docker.com/repository/docker/buluma/opensuse/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|focal, bionic|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-zabbix_repository/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)

Please consider [sponsoring me](https://github.com/sponsors/buluma).

### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
