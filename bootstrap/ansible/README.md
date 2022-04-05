# Configure the OS


1. Install Ansible 
~~~
apt install ansible
apt install sshpass (if required) 
~~~

# Create ssh keys or copy the public key to .ssh/
~~~
ssh-keygen 
copy <pub>  ~/.ssh/id_rsa.pub
~~~

# Verify the hosts
~~~
cat ./hosts
~~~

# Create the 'k8s' user on the servers using ansible
~~~
ansible-playbook k8s-init.yml -u <existing user> -k -K
~~~

# Verify connectivity to all servers 
~~~
ansible -m ping cluster
~~~

# Prepare and setup of kubernetes
~~~
ansible-playbook k8s-setup.yml 
~~~
