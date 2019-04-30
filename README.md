MTO Ansible Role: EPEL Repository
=========

Installs the [EPEL repository](https://fedoraproject.org/wiki/EPEL) (Extra Packages for Enterprise Linux) for RHEL/CentOS.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    repo-epel_url: "http://download.fedoraproject.org/pub/epel/{{ ansible_distribution_major_version }}/{{ ansible_userspace_architecture }}{{ '/' if ansible_distribution_major_version < '7' else '/e/' }}epel-release-{{ ansible_distribution_major_version }}-{{ epel_release[ansible_distribution_major_version] }}.noarch.rpm"
    repo-epel_gpg_key_url: "/etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"

The EPEL repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you need a very specific version, these can both be overridden.


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: mto79.repo-epel }

License
-------

BSD

Author Information
------------------

This role was created in 2019 by [MTO](https://www.mto.nu/).
