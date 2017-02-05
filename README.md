# ansible-centreon

##Centreon version 2.8.x Infrastructure (Central - Poller - Db Server) deployment

- Requires Ansible 2.2 or newer
- Expects CentOS/RHEL 6.x hosts

These playbooks were tested on CentOS 6.x so we recommend
that you use CentOS or RHEL to test these modules.

These playbooks can deploy a simple all-in-one Centreon server or a distributed 
infrastructure with on Central, many Pollers and a dedicated Db server. The 
inventory file 'hosts' defines the nodes in which the stacks should be configured.

        [central]
        central

        [poller]
        poller1
        poller2

        [dbserver]
        db

The stack can be deployed using the following command:

        ansible-playbook -i hosts site.yml

