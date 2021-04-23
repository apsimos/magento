# magento2 role for Ansible
Tested on Centos 7 host with selinux mode - disabled

### Overview of role tasks
* Install and configure NGINX
* Install and configure php-fpm 7.0
* Install and add to path Composer
* Create Magento 2 CE project with composer
* Setup NGINX vhosts as per magento dev docs recommendations
* Install and configure MariaDB
* Install elasticsearch
* Install and configure Redis In-Memory DB
* Install Magento 2 CE using CLI
* Setup Magento 2 Cron jobs

### Installation
Modify parameters on deploy.yml with your data
Fill the 
magento_account_public_key: ""
magento_account_private_key: ""

Also modify inventory file and Vagrant if you want to use VM Local environment

### Run
vagrant up -d

### Add example.com to your hosts file
sudo sh -c "echo '192.168.33.10 example.com'  >> /etc/hosts"

### Then 
ansible-playbook deploy.yml -i inventory/hosts
