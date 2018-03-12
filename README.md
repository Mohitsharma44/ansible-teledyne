Role Name
=========

Ansible role for installing Teledyne Dalsa SDK (tested with v2.02.0.0132)
> Although this role has been tested with v2.02.0.0132 their installer scripts have not changed
> so this is definitely backwards compatible and hopefully even with their new sdk version releases

Requirements
------------

NA

Role Variables
--------------

```yaml

# Dependencies for teledyne sdk
teledyne_deps:
  - g++
  - libgtk-3-dev
  - make
  - libglade2-0
  - libglade2-dev
  - libx11-dev
  - libxext-dev

# If you provide a custom sdk url, make sure to provide sha256 checksum
teledyne_sdk_url: http://localhost:8000/gige-v-framework_20200132.tar.gz
teledyne_sdk_sha256: sha256:a7d25f0616e333e68005cf54ef425252b6ac80388d2d283bafd9864dd3fe3aaa

# Path where you want to download all the SDK files
teledyne_build_dir: "/home/mohitsharma44/teledyne_build"

# Path where you want to keep SDK related installation files
teledyne_install_loc: "/home/mohitsharma44/teledyne_install"

```

Dependencies
------------

NA

Example Playbook
----------------

```yaml
---

- hosts: localhost
  tasks:
  roles:
    - { role: mohitsharma44.ansible-teledyne }
```

License
-------

MIT

Author Information
------------------

Mohit Sharma (Mohitsharma44@gmail.com)
