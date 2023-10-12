Ansible Role: Backblaze
=========

An Ansible role to back up an SMB share via Backblaze Personal.

Requirements
------------

Some user interaction for installing Dokany and Backblaze on the Windows host.

Role Variables
--------------

```yml
smb_host: truenas01.mgmt.bufu-sec.com
smb_username: user
smb_password: Password!
shares:
  - name: tank
    drive_letter: 'z'
defender_exclusions:
  - 'Z:\'
  - '\\10.10.10.9\*'
  - '\\10.10.10.9\tank\*'
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: xbufu.backblaze
           vars:
            smb_host: truenas01.mgmt.bufu-sec.com
            smb_username: user
            smb_password: Password!
            shares:
              - name: tank
                drive_letter: 'z'
            defender_exclusions:
              - 'Z:\'
              - '\\10.10.10.9\*'
              - '\\10.10.10.9\tank\*'

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
