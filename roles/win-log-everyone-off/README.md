win-log-everyone-off
=========

Logs off all disconnected sessions from the targeted server. Shows changed with RC=0 (when someone is actually logged off). Displays no change when RC=1 (no changes were made)

Requirements
------------

None

Role Variables
--------------

all_users: No default. When defined will log everyone off including logged-in users

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }