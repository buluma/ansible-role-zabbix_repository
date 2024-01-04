# Ansible role [zabbix_repository](https://galaxy.ansible.com/ui/standalone/roles/buluma/zabbix_repository/documentation)

Install and configure zabbix_repository on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-zabbix_repository/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-zabbix_repository/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-zabbix_repository.svg)](https://github.com/buluma/ansible-role-zabbix_repository/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/zabbix_repository)](https://galaxy.ansible.com/ui/standalone/roles/buluma/zabbix_repository/documentation)|

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
zabbix_repository_version_major: "6.4"

# The `zabbix_version_minor` is a single numerical value.
zabbix_repository_version_minor: 1

# An extra package is required for RHEL9 (`crypto-policies-scripts`).
# This variable determines if it should be removed or not.
zabbix_repository_cleanup_requirements: yes

# The crypto policy must be modified on RHEL9. This variable determines if
# the policy should be switched back to the default.
zabbix_repository_revert_crypto_policy: yes
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.ca_certificates](https://galaxy.ansible.com/buluma/ca_certificates)|[![Ansible Molecule](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-ca_certificates.svg)](https://github.com/shadowwalker/ansible-role-ca_certificates)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-zabbix_repository/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|8|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|bullseye|
|[opensuse](https://hub.docker.com/repository/docker/buluma/opensuse/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|focal|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-zabbix_repository/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-zabbix_repository/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

