szorfein.privacy.os
===================

A collection to enhance the privacy of your OS (GNU/Linux).

- Change the machine-id.
- Change the hostname.
- Spoof the MAC address.

Requirements
------------

ansible

Role Variables
--------------

- `os_fix_mac_spoof`
  - Default: `true`
- `os_fix_machine_id`
  - Default: `true`
- `os_fix_hostname`
  - Default: `true`
- `os_machine_id`
  - Default: `[b08dfa6083e7567a1921a715000001fb](https://github.com/Whonix/dist-base-files/blob/master/etc/machine-id)`
- `os_hostname`
  - Default: `host`
- `os_network_prefer_ipv6`
  - Default: `false`
- `os_wifi_client`
  - Default: `Undefined`
  - Description: The wifi client to use if you use a wifi card, only `iwd` or `wpa_supplicant` are supported for now.

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
