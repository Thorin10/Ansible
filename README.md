# Ansible-TD

## Installation

Pour installer Ansible sur votre machine : [https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

`git clone https://github.com/Thorin10/Ansible-TD.git`


## Modification

Dans le dossier host_vars vous devez modifier les `ansible_host: ` pour mettre les ip public de vos machines.

Dans ansible.cfg il faut modifier le `remote_user = ` par le nom de votre utilisateur de vos machines.

Dans /playbook/playbook.yml il faut modifier le `remote_user = ` par le nom de votre utilisateur de vos machines.

Dans /playbook/roles/mysql/tasks/main.yml pour l 'étape **Create wordpress user** l 'ip de "host" est l'ip privé de votre VM Database.

Dans /playbook/roles/wordpress/defaults/main.ym. L 'ip de "wp_db_host" est l'ip privé de votre VM Wordpress.

## Lancement

Pour lancer l'installation par les playbooks utilisez:

    `ansible-playbook /playbook/playbook.yml -i ./inventory.ini`

---