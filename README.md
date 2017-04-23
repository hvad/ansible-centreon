# ansible-centreon

##Centreon version 2.8.x Infrastructure (Central - Poller - Db Server) deployment

- Requires Ansible 2.2 or newer
- Expects CentOS/RHEL 6.x hosts

These playbooks were tested on CentOS 6.x so we suggest CentOs or RHEL 
systems usage for module testing.

These playbooks can deploy a simple all-in-one Centreon server or a distributed 
infrastructure with one Central, many Pollers and a dedicated Db server.  
Inventory file 'hosts' defines nodes in which the stacks have to be configured.

        [central]
        central

        [poller]
        poller1
        poller2

        [dbserver]
        db

The stack can be deployed using the following command:

        ansible-playbook -i hosts site.yml

Please note the administrator account of Mariadb has no default password
You must secure the installation of Mariadb.  
SELinux and Firewall have to be disable for a ready-to-work Centreon setup.  

You need to connect to this URL http://ip_address_centreon_web in order to achieve setup.
