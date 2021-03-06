What this project do:
---------------------

* It creates {{ user_name }} user
* It adds {{ user_name }} into /etc/sudoers.d/{{ user_name }}
* It injects the specified public key into the host/s

*It has been tested on RSOE/CSOE 7.6*

Requirements
------------
* ansible version >= "v.2.7". For previous versions the following bug could be experimented: https://github.com/ansible/ansible/issues/44155

How to use it
-------------

* Fill up your inventory file
* Add your public key to the porject folder
* Set the following configurations:

*main.yml:*
```yaml
hosts: #yourTargetGroup/host
vars:
    user_name: #UserToBeCreated
    pubkey: #yourPubKey
```

*ansible.cfg:*
```.yaml
remote_user = #sshUserWithSudoRights
```

Execution example
------------------

```bash
ansible-playbook main.yml 
```

Author Information
------------------

Developed by Adrian Sanchez Medina (adrime92@gmail.com)

If you wish to contribute do not hesitate and raise a pull request, they are more than welcome!

