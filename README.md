# Jenkins-install-via-Ansible

Using Ansible, you can follow the steps below to perform Jenkins installation. These steps are directed to the Ubuntu operating system. If you are using another operating system, you must adapt the steps using the appropriate package manager and service management.

Ansible installation:
First you need to install Ansible in your control machine. You can install Ansible using the following commands in your control machine.

$ sudo apt update
$ sudo apt install -y ansible

Creating an Inventory File:
You must create a "Inventory" file to specify target machines using Ansible. An example inventory.ini file:

[jenkins]
jenkins-server ansible_host=TARGET_IP_ADDRESS ansible_user=REMOTE_USER ansible_ssh_private_key_file=/path/to/private/key.pem

Target_IP_Address and Remote_user values must be replaced by the IP address and user name of the target server you want to install Jenkins. You should also specify the file path of your SSH special key.

Playbook creation:
Create an Ansible Playbook to install Jenkins. An example install_Genkins.yml file:

This PlayBook will install the Java JDK required for Jenkins, some auxiliary packages, Jenkins's APT tank and Jenkins package.

Jenkins installation with Ansible:
You can use the following command to run the PlayBook you created:

$ ansible-playbook -i inventory.ini install_jenkins.yml


This command will install Jenkins on the target machine in the specified Inventory file.

I hope these steps help!

