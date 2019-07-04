Role Name
=========

Role to install Ansible Tower

Requirements
------------

A valid Ansible Tower license needs to be placed into an appropriate `files` directory.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

    # Defaults to use /root. Change to fit your environment
    towerinstall_working_location: /root

    # Define all passwords Tower uses
    # NOTE: Use of Ansible Vault recommended here
    towerinstall_admin_password: "password"
    towerinstall_pg_password: "password"
    towerinstall_rabbitmq_password: "password"

    # Tower Installer
    # Define Tower version to download
    towerinstall_tower_release_version: 3.5.0-1
    # Define http server/path which hosts setup files
    towerinstall_tower_releases_url: https://releases.ansible.com/ansible-tower/setup/
    # The Tower setup file to download
    towerinstall_tower_setup_file: ansible-tower-setup-{{ towerinstall_tower_release_version }}.tar.gz

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: localhost
  vars:
  towerinstall_admin_password: "my_secure_password"
  towerinstall_pg_password: "my_secure_password"
  towerinstall_rabbitmq_password: "my_secure_password"

  roles:
     - role: kenhitchcock.towerinstall

License
-------

BSD

Author Information
------------------

Ken Hitchcock [Github](https://github.com/kenhitchcock)
