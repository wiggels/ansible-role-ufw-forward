UFW Forward
=========

Configure port forwarding in UFW

Requirements
------------

UFW needs to be installed and enabled.
This role currently supports Ubuntu 20.04 and 22.04.

Role Variables
--------------

Port forwarding settings are required as a list under:
    ufw_forward
See the example below for further explaination.

Dependencies
------------


Example Playbook
----------------

You must either be root or `become: yes` in order to 

    - hosts: all
      tasks:
        - name: Configure port forwarding
          ansible.builtin.include_role: 
            name: wiggels.ufw_forward
          vars:
            - ufw_forward_interface: ens192
            - ufw_forward_rules:
                - src_ip: 10.0.0.1
                  src_port: 80
                  dst_ip: 127.0.0.1
                  dst_port: 8080

License
-------

MIT

Author Information
------------------

Hunter Wigelsworth
[GitHub](https://github.com/wiggels)
[LinkedIn](https://www.linkedin.com/in/wiggels/)
[Twitter](https://www.twitter.com/wiggels/)
[Facebook](https://www.facebook.com/wiggels/)