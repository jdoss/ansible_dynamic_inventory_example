## Ansible dynamic EC2 inventory w/ static groups of dynamic groups w/ inventory group_vars example

This is an example of setting up a multi-environment dynamic EC2 inventory with:

* Many different environments
* Many groups in each environment
* Different variables for each environment
* Static groups of dynamic children
* All that use inventory group_vars

The inventory is split up into three different environments. There are two different groups, web and db. The all group is for all groups. The `main.yml` in each group holds non-secret variables and the `vault.yml` holds the encrypted secrets.

The example playbook simply prints out the debug statements for each group and based on what inventory is used, it will load a different set of variables. The links below detail out the best practices followed for setting up the inventory directory structure and how to use static groups of dynamic groups.

http://docs.ansible.com/ansible/playbooks_best_practices.html#alternative-directory-layout
http://docs.ansible.com/ansible/intro_dynamic_inventory.html#static-groups-of-dynamic-groups
