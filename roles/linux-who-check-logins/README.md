linux-who-check-logins
=========

uses the who command (abbreviated to just w) to check and display logged in users

Requirements
---------

Needs to have the following set in ansible.cfg to display correctly:
callback_whitelist = debug
stdout_callback = debug