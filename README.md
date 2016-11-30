Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

### defaults/main.yml

```yaml

---
# defaults file for ansible-role-research_workstation

## required
#
# 

fsl_state             : 'present'   # absent

## Future
#
#fsl_type              : 'full'      # full, free
#fsl_repository_source : us-nh       # us-nh, us-tn, ??

### Debian specific
#
#
#fsl_repositories      : [
                          - 'deb http://neuro.debian.net/debian data main contrib non-free'
                          - '#deb-src http://neuro.debian.net/debian data main contrib non-free'
                        ]

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
