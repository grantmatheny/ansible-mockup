# ansible-mockup
- This is a set of my Windows and Linux update roles and playbooks, along with a minimal example config file

# Setting up
- set up an ssh keypair and set it up with your user on each linux server
- make sure to set up /etc/krb5.conf to point to your AD
- DNF packages: krb5-devel, krb5-workstation, python3, python3-pip, git, gcc, python3.x-devel
- pip installs as root: pyvmomi, pypsexec, pywinrm[kerberos]
- pip installs as user: jmespath, smbprotocol[kerberos], boto3
- community.vmware Ansible collection (install with $ansible-galaxy collection install community.vmware)
- put the ansible vault password into a file as specified in the "vault_password_file" in ansible.cfg, and all the rest of the encrypted files will use that password to decrypt. All other files are checked into Git, with secret files encrypted. To edit those files, use ansible-vault edit <filename> in a fully-set-up ansible installation, and they'll open in your default editor.
- Vi is often the editor by default. Change your editor by putting "export EDITOR=nano" (or another editor in place of 'nano') in your .bashrc.
