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

# Run Playbook as Vagrant User
ansible-playbook playbook.yaml -u vagrant
# Dry run as Vagrant User 
ansible-playbook playbook.yaml -u vagrant --check

