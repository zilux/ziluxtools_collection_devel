# Ansible Collection - zilux.tools

Documentation for the collection.

check out for testing: (not for code writing)

$ ansible-galaxy collection install git@github.com:zilux/ziluxtool_collection.git -p ./collections


example how to use this:


```
---
- name: basehost ( baseline a host )
  hosts: all
  gather_facts: true
  become: true
  tasks:

  roles:
    - zilux.tools.bootstrap
    - role: zilux.tools.env_ansible
      env_ansible_user: harry
    - zilux.tools.check

  post_tasks:

  - debug: var=hz_facts
 ```
