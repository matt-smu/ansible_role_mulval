Role Name
=========

Installs MulVal on a system

Requirements
------------

Requires MySQL DB for NVD CVSS lookups. If NVD is needed, run ```ansible-galaxy install -r requirements.txt``` to install MySQL from ansible role. To load the DB add ```mulval_sync_nvd: True``` to your playbook vars. 

Role Variables
--------------

```

# mulval install options
mulval_install_dir: /opt
mulval_home: "{{ mulval_install_dir }}/mulval"

xsb_install_dir: /opt
xsb_home: "{{ xsb_install_dir }}/XSB"

# mulval run options
mulval_sync_nvd: False # load the nvd db (slow)

nvd_db_user: nvd
nvd_db_pass: nvd
nvd_db_schema: nvd
```

Dependencies
------------

```src: https://github.com/geerlingguy/ansible-role-mysql.git
```
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: mulval }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
