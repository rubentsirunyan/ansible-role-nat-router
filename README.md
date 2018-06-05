Ansible Role: nat_router
=========

This role sets up a simple NAT router on a Linux machine that can act as a default gateway for the local network to the Internet.

Requirements
------------

None.

Role Variables
--------------

`public_interface`: The name of the network interface that faces to the public network (Internet). The default value is `eth0` 
`private_interface`: The name of the network interface that faces to the local/private network. The default value is `eth1` 

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: linux_routers
      roles:
        - role: rubentsirunyan.nat_router
          vars:
            - public_interface: enp0s3
            - private_interface: eth0

License
-------

BSD

Author Information
------------------

This role is created by Ruben Tsirunyan https://github.com/rubentsirunyan