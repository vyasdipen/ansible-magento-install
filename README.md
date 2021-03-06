# Ansible - Install Magento 2 on Nginx

This ansbile script works for Nginx only. It will allows you to setup magento2 community edition on system. It will reduce manual efforts to install fresh magento 2 on your local system. Once installation will be done, link will open in google chrome or you can also try to access it using  `projectname.site`. 

This is just a basic script for Nginx. 

## System Requirments

1. Operating System Linux distributions (such as RedHat Enterprise Linux (RHEL), CentOS, Ubuntu, Debian, and similar)

2. Ansible [How to install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

3. Nginx [How to install Nginx](https://ubuntu.com/tutorials/install-and-configure-nginx#1-overview)

4. Magento compatible configuration [Check system requirment for Magento2](https://devdocs.magento.com/guides/v2.3/install-gde/system-requirements-tech.html)

## How to use

1.  git clone or download this script.

2. Go to directory `ansible-magento-install`

3. run following command 
	```sh
	ansible-playbook magento2.yml  --ask-become-pass
	```

4.  I recommend to run it with argument  `--ask-become-pass` to prevent script failure and handle sudo privilages. 

5. Once installation will be completed, it will auto launch the site in chrome browser or you can access it using url projectname.site 

## Troubleshoot

1. Instad of running it using sudo command, I recommend run it using argument "--ask-become-pass"  
2. Can not connect to localhost: 
Ans:  In that case  you need to enter the host entry in to the ansible host file.To do so, edit /etc/ansible/hosts file or create new inventory file in ansible directory.  Add following entry and save the file.

```sh
[localhost]
localhost ansible_connection=local
```
