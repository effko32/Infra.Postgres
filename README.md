# Infra.Postgres

Deploy HA-Cluster PostgreSQL:
  1. HAProxy
  2. etcd
  3. Patroni
  4. PostgreSQL

ansible-playbook ha-cluster.yml -i hosts/inventory.ini -e "ansible_ssh_pass=$(rootPassword)" -e "ansible_become_pass=$(rootPassword)" -e "postgres_root_pass=$(postgres_root_pass)" -e "target=all"

ansible-playbook ha-cluster.yml -i hosts/inventory.ini -e "ansible_ssh_pass=$(rootPassword)" -e "ansible_become_pass=$(rootPassword)" -e "postgres_root_pass=$(postgres_root_pass)" -e "target=all" --tags "haproxy"

https://github.com/effko32/Infra.Postgres