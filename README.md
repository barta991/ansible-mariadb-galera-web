# ansible-mariadb-galera-web
Ansible scripts to deploy MariaDB cluster with any number of nodes

## Requirements
1) ansible 1.9.2 (Only tested on this version)
2) Password-less ssh access to the nodes and sudo access for the user. (As always)
3) Currently developed only for Ubuntu, will try to complete it for Redhat/CentOS as well. 

## Usage
Edit the inventory file with correct IPs and database password.

**Note:** The first node will be used for bootstrapping. After it is done and the nodes are joined, the first node's service is again restarted normally (without bootstrap).

```# ansible-playbook site.yml -i inventory -become```


