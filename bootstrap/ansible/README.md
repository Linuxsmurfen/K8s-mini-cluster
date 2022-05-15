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

3. Verify/edit the hosts file
~~~
vi ./hosts
~~~

4. Create the *remote_user* on the servers using ansible
~~~
ansible-playbook k8s-init.yaml -u <existing user> -k -K
~~~

5. Verify connectivity to all servers 
~~~
ansible -m ping nodes
~~~



# Create the Kubernetes cluster

Prepares the servers and installs Kubernetes via kubeadm.
~~~
ansible-playbook k8s-setup.yaml 
~~~




# Wipe the Kubernetes cluster
~~~
ansible-playbook k8s-wipe.yaml 
~~~
