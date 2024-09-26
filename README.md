# graylog-installer
Graylog 6 installer for Ubuntu 22.04

This playbook will install all parts to get Graylog set up.

It will install and configure:

MongoDB
Opensearch
Graylog-server
install password
salted and hashed passwords
sets correct values in cfg files for both Opensearch and Graylog


Variables:

cluster_name= this will be the name of the cluster if you choose to create one
remote-user=this is the local user that has to run sudo to install $things


Syntax:

ansible-playbook -i inventory.ini graylog-installer.yml --ask-pass --extra-vars 'cluster_name=graylog-cpe remote_user=<remote-user>'
