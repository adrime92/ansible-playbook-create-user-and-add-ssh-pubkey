# Role:
This role:
* Creates {{ user_name }} user
* Adds it into /etc/sudoers.d/{{ user_name }}
* Export the specified pub.ssh

## Example Execution

Clustering:

```sh
ansible-playbook main.yml -i inventory -u {{ user }} --ask-pass 
```