Ansible Role WireGuard
=========

This role installs and configures WireGuard on Ubuntu 20.04+.

Requirements
------------

Operating System Support: Ubuntu 20.04 or later

Role Variables
--------------

# Server Config
```
wg_mode: server
# wg_server_client_network: 192.168.100 # .1/24 will be auto assigned
wg_server_service_port: 51820
wg_server_interface_number: 0
wg_server_public_interface: "{{ ansible_default_ipv4['interface'] }}"
```

Dependencies
------------

No dependency.

Example Playbook
----------------

Install
```
ansible-galaxy install cihanyilmazer.ansible_role_wireguard
```

    - hosts: servers
      roles:
         - cihanyilmazer.ansible_role_wireguard/server

Run with Custom Tags (at least one tag must be provided)
- wireguard
- wireguard-install
- wireguard-configure-tunnel
- wireguard-configure-ufw

```
ansible-playbook -i hosts playbook.yml --tags initial --limit servers
```

License
-------

MIT

Author Information
------------------

Cihan Yilmazer<br />
https://www.cihanyilmazer.com<br />
https://www.github.com/cihanyilmazer<br />
https://galaxy.ansible.com/cihanyilmazer<br />