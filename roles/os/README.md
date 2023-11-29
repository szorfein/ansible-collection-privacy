Role Name
=========

+ Anonymize the unique machine ID identifier.
+ Use generic value for identifiers like hostname=host, timezone=utc, etc...

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- `os_hostname:`
   - Default: `false`
   - Description: Change or not the value of hostname.
   - Type: bool
- `os_hostname_value:`
   - Default: `'host'`
   - Description: The new value for hostname.
   - Type: str
- `os_hostname_list:`
   - Default: `[]`
   - Description: If other hosts to add on /etc/hosts. e.g: ["192.168.1.1 router", "14.13.144.120 superhost"]
   - Type: list
- `os_machine_id:`
   - Default: `false`
   - Description: Erase or not the default unique ID.
   - Type: bool
- `os_machine_id_value:`
   - Default: `b08dfa6083e7567a1921a715000001fb`
   - Description: Each machine has a unique id (man machine-id). We use by default the same ID than Whonix.
   - Type: str
- `os_mac_change:`
   - Default: `false`
   - Description: Make your MAC address random (by NIC) by using macchanger.
   - Type: bool
- `os_timezone:`
   - Default: `false`
   - Description: Change timezone.
   - Type: bool
- `os_timezone_value:`
   - Default: `'UTC'`
   - Description: Set timezone to UTC by default. With systemd, see `timedatectl list-timezones`.
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
