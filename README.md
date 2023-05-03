# [software](#software)

Install or uninstall software on your system.

|GitLab|Quality|Downloads|Version|
|------|------|-------|---------|-------|
|[![gitlab](https://gitlab.collegis.corp/dustinliddick/ansible-role-software/badges/master/pipeline.svg)](https://gitlab.collegis.corp/dustinliddick/ansible-role-software)|[![quality](https://img.shields.io/ansible/quality/51260)](https://galaxy.ansible.com/dustinliddick/software)|[![downloads](https://img.shields.io/ansible/role/d/51260)](https://galaxy.ansible.com/dustinliddick/software)|[![Version](https://img.shields.io/github/release/dustinliddick/ansible-role-software.svg)](https://github.com/dustinliddick/ansible-role-software/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/dustinliddick/ansible-role-software/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: dustinliddick.software
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/dustinliddick/ansible-role-software/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: dustinliddick.bootstrap
```

Also see a [full explanation and example](https://dustinliddick.nl/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/dustinliddick/ansible-role-software/blob/master/defaults/main.yml):

```yaml
---
# defaults file for software

# A list of software packages to manage.
# software_packages:
#   - name: screen
#   - name: tcpdump
#     state: absent
software_packages: []
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/dustinliddick/ansible-role-software/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[dustinliddick.bootstrap](https://galaxy.ansible.com/dustinliddick/bootstrap)|[![Build Status GitHub](https://github.com/dustinliddick/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/dustinliddick/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/dustinliddick-iac/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/dustinliddick-iac/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://dustinliddick.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/dustinliddick/ansible-role-software/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/dustinliddick):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/repository/docker/dustinliddick/enterpriselinux/general)|8|
|[Fedora](https://hub.docker.com/repository/docker/dustinliddick/fedora/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/dustinliddick/ansible-role-software/issues)

## [License](#license)

[Apache-2.0](https://github.com/dustinliddick/ansible-role-software/blob/master/LICENSE).

## [Author Information](#author-information)

[dustinliddick](https://dustinliddick.nl/)

Please consider [sponsoring me](https://github.com/sponsors/dustinliddick).
