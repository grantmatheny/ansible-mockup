win-wu-universal
=========
Installs or checks for windows updates

Requirements
------------

None

Role Variables
--------------

wu_state: searched (can be set to "installed")
wu_categories: (can be set to a single one of the below without dashes)
  - SecurityUpdates
  - CriticalUpdates
  - UpdateRollups
  - Application
  - DefinitionUpdates
  - FeaturePacks
  - Updates
  - Connectors
  - Tools
  - Drivers
wu_reboot: no (set to "yes" to allow reboot as part of installation)
wu_force_detection: "yes" (goes through a forced detection)
wu_check_reboot: no (if yes and state set to searched, only checks to see if a reboot is required)

Dependencies
------------

None

Example Playbook
----------------

---
- hosts: "{{ target }}"
  name: Install Updates and Reboot
  vars_prompt:
    - name: target
      prompt: "Enter host(s) or group(s), comma-separated"
      private: no
  vars:
    wu_reboot: "yes"
    wu_state: "installed"
    all_users: true
  roles:
    - role: win-logons
      vars:
        logon_state: disabled
    - win-log-everyone-off
    - role: win-bitlocker
      vars:
        bitlocker_state: suspend
    - win-choco-update-install
    - win-wu-universal
    - role: win-bitlocker
      vars:
        bitlocker_state: resume
    - win-logons
      vars:
        logon_state: enabled