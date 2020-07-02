win-wsus
=========

Checks for and optionally Approves all updates on the WSUS server for the computer group specified in wsus_classification

Requirements
------------

WSUS installed and configured on target machine.

Role Variables
--------------

wsus_classification: defaults to All Computers
wsus_approve: when defined, will actually approve specified updates

Dependencies
------------

None.

Example Playbook
----------------

- hosts: <wsus server>
  roles:
    - win-wsus
  vars: 
    wsus_classification: <Server Group>
    wsus_approve: true

