# Ansible Role to Install LXC 2 on Centos and Build LXC Containers

This role will allow you to install LXC 2 on Centos 7 and then build a series of containers that you have listed in your inventory file.


## Role Variables

This role does not have any variables

The list of containers to build is taken directly from your inventory, by looping over all hosts in the group `lxc`

## Dependencies

This role uses COPR to install modern LXC on Centos 7 and so has a dependency on https://galaxy.ansible.com/edmondscommerce/copr-repository/

## Example Inventory

```
[web]
cnt-web-1

[db]
cnt-db-1
                                                                                                                                                                                                                   
[lxc]
cnt-web-1
cnt-db-1
```

## Example Playbook

```
- name: install lxc and create lxc containers
  hosts: localhost
  become: true
  roles:
      - lxc-create
```


## License

Apache

## Author Information

[Edmonds Commerce](https://www.edmondscommerce.co.uk) are a UK based PHP development agency specialising in E-Commerce and Magento.

https://www.edmondscommerce.co.uk
