https://devopsideas.com/ansible-local-setup-using-vagrant-virtualbox/

# Vargrant Commands
vargrant up - spin up vm (uses vagrant file from current directory)
vargrant status - lists current available vagrant made vms
vagrant ssh <vm name> - ssh into vm

# Ansible
sudo yum install ansible
sudo vim /etc/ansible/hosts
add ssh keyfrom localmachine to ~/.ssh/authorized_keys
ansible app -m ping -u vagrant - ping vm

# Download required installers (.rpm, .run, .deb) into appropiate playbook (see vars in playbook for context)
# Edit vars in appropiate playbook to match installer names
# Run Playbook as Vagrant User
ansible-playbook playbook.yaml -u vagrant
# Dry run as Vagrant User
ansible-playbook playbook.yaml -u vagrant --check

# Run Playbook on local host
# Uncomment "hosts: localhost" and "connection: local" in playbook
# Comment out  "hosts: apps" in playbook 
