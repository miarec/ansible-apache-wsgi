# ansible-apache-wsgi

Ansible role to install mode_wsgi apache module from source code


Role Variables
--------------

- `wsgi_version`: The version of mod_wsgi module to install
- `python_version`: The version of python to compile the mod_wsgi with
- `python_install_dir`: The location of python installed files (default is /usr/local)
- `wsgi_force_install`: Install again even if the mod_wsgi is already installed as an apache module

See `defaults/main.yml` for more variables


Example Playbook
----------------

eg:

``` yaml
    - name: Install apache mod_wsgi module
      hosts: localhost
      become: yes
      roles:
        - role: ansible-apache-wsgi
          wsgi_version: 4.4.21
          python_version: 3.5.3
```

The above playbook will install mod_wsgi module v.4.4.21 compiled python version 3.5.3.

Requirements
------------

- Apache - It should be already installed
- Python - It should be already installed


