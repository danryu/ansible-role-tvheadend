Ansible Role: Tvheadend
=========
[![Build Status][travis_badge]][travis_results]

Installs and configures [Tvheadend][tvheadend].

Requirements
------------

```shell
# Ansible version 1.6+
ansible --version

# OS
case $OSTYPE in
  # Linux needs apt
  "linux"*)
      apt --version;;
esac
```

Role Variables
--------------

```yaml
tvheadend_username: admin
tvheadend_password: admin

tvheadend_apt_key: "http://apt.tvheadend.org/repo.gpg.key"
tvheadend_apt_repo: "deb http://apt.tvheadend.org/unstable trusty main"
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers.media
  roles:
    - name: ensure Tvheadend
      role: cmprescott.tvheadend
```

License
-------

BSD

Author Information
------------------

Based off Gregory Shulov's [htpc-ansible][htpc-ansible] playbook. Updated and maintained by Prescott Chris.

[htpc-ansible]: https://github.com/GR360RY/htpc-ansible
[tvheadend]: https://tvheadend.org/
[travis_badge]: https://travis-ci.org/cmprescott/ansible-role-tvheadend.svg?branch=master
[travis_results]: https://travis-ci.org/cmprescott/ansible-role-tvheadend