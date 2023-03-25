# ansible-install-ubuntu

## 1. Ansible on ubuntu machine. 

sudo apt-get update -y

sudo apt install -y software-properties-common

sudo add-apt-repository --yes --update ppa:ansible/ansible

sudo apt update

sudo apt install -y ansible

ansible --version

- - - 
On Hosts - 

sudo apt-get update
sudo apt-get install python

python3 --version

- - -

## 2. Configure SSH Access to Ansible Host machines

On the controller, generate ssh key using    -         ssh-keygen

Copy the  id_rsa.pub to the host .ssh/  authorized_keys

And now should be able to ssh into the host from the controller 

## 3. Setting up Ansible Host and testing connection 

Exit from the host back to the controller 

sudo nano /etc/ansible/hosts 

Add to the bottom of the file 
[production]
agent1 ansible_ssh_host=172.31.43.43

