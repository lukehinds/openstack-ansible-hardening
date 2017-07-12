# WARNING ! WIP DO NOT USE!

OpenStack Ansible Hardening
=========================

Ansible role to perform OpenStack service hardening, based on the OpenStack security guide.

Role Variables
--------------

Roles specific to a release can be performed with a tag.

For example `ansible-playbook playbook.yaml --tags newton`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: OpenStack Ansible Hardening
      hosts: all
      become: yes
      roles:
        - openstack-ansible-hardening

License
-------

Apache 2.0

Author Information
------------------

Luke Hinds (lhinds@redhat.com)
