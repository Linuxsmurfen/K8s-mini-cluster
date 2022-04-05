# Configure the OS


1. Install Ansible 
~~~
apt install ansible
apt install sshpass (if required) 
~~~

2. Create a ssh keys or copy the public key to .ssh/
~~~
ssh-keygen 
copy <pub>  ~/.ssh/id_rsa.pub
~~~

3. Verify the hosts
~~~
cat ./hosts
~~~

4. Create the 'k8s' user on the servers using ansible
~~~
ansible-playbook k8s-init.yml -u <existing user> -k -K
~~~

5. Verify connectivity to all servers 
~~~
ansible -m ping nodes
~~~

6. Prepare and setup of kubernetes
~~~
ansible-playbook k8s-prepare.yml 
~~~
