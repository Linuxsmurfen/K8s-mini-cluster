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
ansible-playbook k8s-init.yml -u <existing user> -k -K
~~~

5. Verify connectivity to all servers 
~~~
ansible -m ping nodes
~~~



# Kubernetes setup

Prepares the servers and installs Kubernetes via kubeadm.
~~~
ansible-playbook k8s-setup.yml 
~~~




# Remove Kubernetes

~~~
kubeadm reset
rm -rf $HOME/.kube
sudo rm -rf /etc/cni/net.d
sudo iptables -F && sudo iptables -t nat -F && sudo iptables -t mangle -F && sudo iptables -X

sudo apt-get purge kubeadm kubectl kubelet kubernetes-cni kube*   
sudo apt-get autoremove  
~~~
