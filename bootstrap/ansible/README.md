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



# Kubernetes setup

1. Install Kubeadm and adjust the servers
~~~
ansible-playbook k8s-prepare.yml 
~~~

2. Setup the ControlPlane node

3. Setup the Worker nodes



# Remove Kubernetes

~~~
sudo kubeadm reset
rm -rf $HOME/.kube
sudo rm -rf /etc/cni/net.d
sudo iptables -F && sudo iptables -t nat -F && sudo iptables -t mangle -F && sudo iptables -X
~~~
