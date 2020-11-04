Role Name
=========

This role will add a user and their public ssh keys to a server and assign an account password. It also adds the user to /etc/ssh/sshd_config AllowedUsers list. 

Be careful not to lock yourself or others out of servers with this role. If you comment users in default vars, it will re-render the sshd_config template and that user will be locked out. You have been warned.

Role Variables
--------------

Example of variable structure:

  - { name: gmcmillan, key: "{{ lookup('file', 'gmcmillan.pub')}}", password: password123 }

Dependencies
------------

No dependencies necessary.
