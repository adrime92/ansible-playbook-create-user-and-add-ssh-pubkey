# Role:
This role:
* creates {{ user_name }} user
* adds {{ user_name }} into /etc/sudoers.d/{{ user_name }}
* injects the specified pub.ssh (add .pub in the project folder)
* has been tested on RSOE/CSOE 7.6 (maipo)

## How to use it

Set the following configurations:

**main.yml:**
```yaml
hosts: #yourTargetGroup/host
vars:
    user_name: #UserToBeCreated
    pubkey: #yourPubKey
```

**ansible.cfg:**
```.yaml
remote_user = #sshUserWithSudoRights
```

**Fill up your inventory file**

## Example Execution

```bash
ansible-playbook main.yml 
```