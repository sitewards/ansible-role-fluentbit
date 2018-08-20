Role Name
=========

A brief description of the role goes here.

## Requirements

There are no special requirements to this role

## Variables

Variables that can be customised in this role are documented in `defaults/main.yml`

## Dependences

This role has no other dependencies

## Installation

### Ansible Galaxy (recommended)

```bash
$ cd path/to/playbook/root
$ cat >> requirements.yaml <<EOF
- src: "https://github.com/sitewards/ansible-role-fluentbit.git"
  version: "master" # <----- Update this to a stable version
  name: "sitewards.fluentbit"
EOF
$ ansible-galaxy install -r requirements.yaml
```

### Git Submodules

```
$ cd path/to/playbook/root
$ mkdir roles/
$ git submodule add https://github.com/sitewards/ansible-role-fluentbit.git sitewards.fluentbit
```


## Usage

Include this in another ansible playbook. For sample, consider a generic server playbook:

```
---
# $PLAYBOOK_ROOT/server.yaml
- name: "server"
  hosts: all
  become: true
  become_user: "root"
```

Add the reference for the role:

```
# $PLAYBOOK_ROOT/server.yaml
# ...
become_user: "root"
roles
  - "sitewards.fluentbit"
```

This should work!

## License

OSL-3.0

## Author Information

- Behrouz Abbasi
- Andrew Howden
