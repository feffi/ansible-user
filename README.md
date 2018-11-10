# ansible-user

Ansible role to configure/add a user.

[![Build Status](https://img.shields.io/travis/feffi/ansible-user.svg)](https://travis-ci.org/feffi/ansible-user) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-user/total.svg)](https://github.com/feffi/ansible-user) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-user.svg?style=social&label=Fork)](https://github.com/feffi/ansible-user) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-user.svg?style=social&label=Star)](https://github.com/feffi/ansible-user) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-user.svg?style=social&label=Watch)](https://github.com/feffi/ansible-user) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-user/blob/master/LICENSE)

## Role Defaults Variables

```yaml
user: {
  name: "feffi",
  password: "SOMEPASSWORD",
  group: "feffi",
  groups: [
    "uucp",
    "wheel",
    "games",
    "rfkill"
  ],
  shell: "/usr/bin/zsh"
}

```

Example:

```yaml
- hosts: all
  vars:
    user:
      name: "feffi"
      password: "SOMEPASSWORD"
      group: "feffi"
      groups:
        - "uucp"
        - "wheel"
        - "games"
        - "rfkill"
      shell: "/usr/bin/zsh"
  roles:
    - { role: ansible-user }
```
