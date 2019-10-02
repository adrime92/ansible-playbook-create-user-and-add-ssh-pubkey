# Role:
This role:
* Creates {{ user_name }} user
* Adds it into /etc/sudoers.d/{{ user_name }}
* Injects the specified pub.ssh (add .pub in the project folder)
* Has been tested on RSOE/CSOE 7.6 (maipo)
## How to use it

Set the following configurations:

*main.yml*:
```yml
hosts: #yourTargetGroup/host
vars:
    user_name: #UserToBeCreated
    pubkey: #yourPubKey
```

*ansible.cfg*:
```.cfg
remote_user = #sshUserWithSudoRights
```

*Fill up your inventory file*

## Example Execution

```sh
ansible-playbook main.yml 
```