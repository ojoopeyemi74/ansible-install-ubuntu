## Create and Inventory file in the controller
## if you dont by default it will be created in /etc/ansible/hosts 

create an Inventory file on the controller
mkdir test-project 
touch inventory.txt

# inside the inventory file specify the targets e.g
target1 ansible_host=172.31.43.43
target2 ansible_host=172.31.42.5

# to text connectivity
ansible all -m ping -i inventory.txt
or 
ansible <target-name> -m ping -i inventory.txt


