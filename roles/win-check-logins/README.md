win-check-logins
=========

Uses the query users command on windows to check which users are logged in. Returns logged in users. 

Requirements
---------
Needs to have the following set in ansible.cfg to display correctly:
callback_whitelist = debug
stdout_callback = debug