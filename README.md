Role Name
=========

Configures a researchers workstation with tools using a standard configuration.

Requirements
------------

### clone role

```shell

cd roles
git clone git@github.com:cjsteel/ansible-role-research_workstation.git research_workstation
cd ..

```

Role Variables
--------------

### project/group_vars

You probably want to overide the roles/research_workstation/defaults/main.yml value for `research_workstation_deployment_user` in `project/group_vars` as follows:

```shell

mkdir -p group_vars/research_workstation
cp roles/research_workstation/files/group_vars/research_workstation/research_workstation_defaults.yml group_vars/research_workstation/.
nano group_vars/research_workstation/research_workstation_defaults.yml

```

#### Content example

```yaml

# group_vars/research_workstation/research_workstation_defaults.yml
#

research_workstation_deployment_user: 'deploy'

```

### defaults/main.yml

* [defaults/main.yml](http://github.com/cjsteel/ansible-role-research_workstation/blob/master/defaults/main.yml)


Dependencies
------------

* [ansible-role-ensure_dirs](https://github.com/csteel/ansible-role-ensure_dirs)

Example Playbook
----------------

### main playbook example

```yaml

---
- hosts: all
  become: false

- include: deployment_user.yml
- include: shorewall.yml
- include: ldap.yml
- include: workstation.yml
- include: research_workstation.yml

```

### research_workstation playbook example

```yaml

---
# project playbook for ansible-role-research_workstation

- hosts: research_workstation
  become: true
  gather_facts: true
  roles:
    - research_workstation
#    - { role: username.rolename, x: 42 }

```

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
