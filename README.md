Refrences
=========
https://medium.com/@jmarhee/creating-a-saltstack-test-environment-with-docker-compose-7dfa79837712
http://phase2.github.io/devtools/common-tasks/ssh-into-a-container/
https://www.digitalocean.com/community/tutorials/saltstack-infrastructure-creating-salt-states-for-nginx-web-servers

Saltstack
=========

A docker-ized Saltstack fleet, for use with training materials. 

Add the number of Salt minions desired in `docker-compose.yml` (add a new object for each new node), then save and deploy:

```bash
$ docker-compose up -d                                                                            
Creating network "saltstack_default" with the default driver
Creating saltstack_salt-master_1
Creating saltstack_salt-minion-3_1
Creating saltstack_salt-minion-2_1
Creating saltstack_salt-minion-1_1
```
After allowing some time for the minions to connect to the master, and the script to accept their keys, you can access the fleet:

```bash
$ docker exec saltstack_salt-master_1 salt "*" test.ping                                          
salt-minion-lonely_kalam:
    True
salt-minion-sick_goodall:
    True
salt-minion-cocky_kirch:
    True
```
