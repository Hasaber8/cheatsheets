# System management

## auto start a service

1. sudo update-rc.d <SERVICE_NAME> defaults
2. sudo update-rc.d <SERVICE_NAME> enable


## LDAP

LDAP is a standardized service to manage hierarchical information.

### Concepts

DN and RDN:


## managing block device

### get the block uuid

```
sudo blkid
```

### get more detailed info of blocks

```
sudo lsblk -f
```

## sudo

remove the password of sudo[^1].

## LVM

http://www.howtogeek.com/howto/40702/how-to-manage-and-use-lvm-logical-volume-management-in-ubuntu/
https://linuxconfig.org/linux-lvm-logical-volume-manager


## firewall manangemment

`uwf`: https://www.cyberciti.biz/faq/how-to-open-firewall-port-on-ubuntu-linux-12-04-14-04-lts/


## java

### installation

http://tipsonubuntu.com/2016/07/31/install-oracle-java-8-9-ubuntu-16-04-linux-mint-18/

## Ref
*[Install OpenLDAP In Ubuntu 15.10 And Debian 8](https://www.unixmen.com/install-openldap-in-ubuntu-15-10-and-debian-8/)
*[OpenLDAP Server](https://help.ubuntu.com/lts/serverguide/openldap-server.html)
*[How To Install and Configure OpenLDAP and phpLDAPadmin on an Ubuntu 14.04 Server](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-openldap-and-phpldapadmin-on-an-ubuntu-14-04-server)

[^1]: http://askubuntu.com/questions/235084/how-do-i-remove-ubuntus-password-requirement
