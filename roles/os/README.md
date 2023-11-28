Role Name
=========

+ Anonymize the unique machine ID identifier.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- `os_machine_id:`
   - Default: `false`
   - Description: Erase or not the default unique ID.
   - Type: bool
- `os_machine_id_value:`
   - Default: `b08dfa6083e7567a1921a715000001fb`
   - Description: Each machine has a unique id (man machine-id). We use by default the same ID than Whonix.
   - Type: str

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: privacy.os, os_machine_id: true }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
