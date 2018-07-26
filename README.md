#### Step 1 - Configure file var/main.yml

- Set the environment variables

#### Step 2 - Inventory 

- open file hosts 

Example:

```bash
[etcd]
10.0.0.10
10.0.0.11
10.0.0.12

[master]
10.0.0.20
10.0.0.21
10.0.0.22

[worker]
10.0.0.30
10.0.0.31
10.0.0.32
10.0.0.34

[all:vars]
ansible_ssh_user=ec2-user
ansible_ssh_private_key_file=~/git/ks8-cluster/terraform/keypair/kubernetesMaster.pem

```

#### Step 3 - Executing playbook Ansible

```bash
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i hosts ./tasks/main.yml --skip-tags etcdrm
```