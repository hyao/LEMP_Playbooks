LEMP Playbooks
=========================

A set of playbooks to deploy LEMP stack on Ubuntu LTS, including MySQL, Nginx, php5-fpm pools. With optional playbooks to deploy Supervisor, Fail2ban, basic ufw firewall setup etc. 

You may need to make some modifications as per your requirements.

To deploy a standard LEMP stack:

```ansible-playbooks deploy.yml```

In more detail:

1. add your host to ansible inventory
2. edit roles/websites/files/sites-{{ hostname }}.yml

```
sites:
  - user: user1 
    dir: site1.example.com 
    php_pool: 9001 
    server_name: site1.starvm.com 

  - user: user2 
    dir: site2 
    php_pool: 9002 
    server_name: site2.example.com
```

3.ansible-playbooks deploy.yml
