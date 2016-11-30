Role Name
=========

Configures a researchers workstation with tools using a standard configuration.

Requirements
------------

* ansible-role-ensure_dirs

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

```yaml

!()[defaults/main.yml]

```
Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
