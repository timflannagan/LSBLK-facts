Purpose
=======
- This is a simple Ansible playbook that installs a custom fact into a controlled host.
- The site.yml file checks whether the /etc/ansible/facts.d directory exists, then creates
  the *.facts on the specified hosts
- The playbook doesn't actually execute the lsblk custom fact, but will present it during 
  the loading process

Commands
========
- $ ansible-playbook -i hosts site.yml --ask-sudo-pass
- $ ansible -m setup localhost "filter=ansible_local" 
or 
- $ ansible -m setup localhost | grep ansible_local