win-bitlocker
=========

Uses powershell resume-bitlocker and suspend-bitlocker to manipulate bitlocker state for all drives. Thanks to reddit user https://www.reddit.com/user/zoredache/ for helping consolidate my on and off roles

Requirements
------------

Bitlocker must be installed

Role Variables
--------------

bitlocker_state: defaults to "resume" but can be set to "suspend" to turn off bitlocker

Dependencies
------------

None.

Example Playbook
----------------

None.
