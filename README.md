#### Step 1 - Configure file var/main.yml

- Set the environment variables

#### Step 2 - Inventory 

- open file hosts

#### Step 3 - Executing playbook Ansible

```bash
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i hosts ./tasks/main.yml --skip-tags etcdrm
```