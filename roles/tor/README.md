szorfein.privacy.tor
====================

- Install and configure Tor (check for [ConnectionPadding](https://www.whonix.org/wiki/Whonix-Gateway_Security#Tor_Connection_Padding), [Sandbox](https://www.whonix.org/wiki/Whonix-Gateway_Security#Seccomp)...).
- Configure package manager to use tor [Arch](https://wiki.archlinux.org/title/Tor#Pacman) - [Void](https://docs.voidlinux.org/xbps/repositories/mirrors/tor.html).
- Use iptables to redirect local traffic throught tor, also disable udp protocol.
- Prevent identity correlation through circuit sharing by using Tor Stream Isolation.
- Install Onionshare.
- Disable NTP and update time with tor.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- `tor`
  - Default: `false`
  - Description: Install and configuring tor and torsocks.
  - Type: bool
- `tor_config_dir`
  - Default: `/etc/torrc.d`
  - Description: Directory used to install configuration.
  - Type: str
- `tor_localhost`
  - Default: `127.0.0.1`
  - Description: Address for the loopback address, normally right.
  - Type: str
- `tor_package_manager`
  - Default: `false`
  - Description: Configure package manager to use tor.
  - Type: bool
- `tor_package_manager_port`
  - Default: `9052`
  - Description: Port to redirect on tor via SocksPort.
  - Type: str
- `tor_stream`
  - Default: `false`
  - Description: Install and configure apps to use different tor circuit.
  - Type: bool
- `tor_stream_port_default`
  - Default: `9050`
  - Description: Port used for default/torsocks stream.
  - Type: str
- `tor_stream_port_curl`
  - Default: `9053`
  - Description: Port used for Curl on socks5.
  - Type: str

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: cloaks
      roles:
         - { role: szorfein.privacy.tor, tor: true }

References
----------

- https://www.whonix.org/wiki/Stream_Isolation
- https://tails.net/contribute/design/stream_isolation/
- https://gitlab.tails.boum.org/tails/tails
- https://www.kicksecure.com/wiki/System_Hardening_Checklist#Tor_Settings
