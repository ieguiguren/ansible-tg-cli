Telegram-cli
============

Downloads and compile telegram-cli with Lua and Python support

Requirements
------------

Role installs everything it needs itself. Actually not working on RedHat-alike distros.

Role Variables
--------------

No variables needed.

Dependencies
------------

This role is standalone and has no dependencies

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: ieguiguren.tg-cli }

License
-------

BSD

Author Information
------------------

Any suggestion, merge request, bug... notify via https://github.com/ieguiguren/ansible-tg-cli
