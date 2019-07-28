# tech-challenge

Requirements:
1.	Use Salt to install NGINX on a debian based linux distribution such as Ubuntu
2.	Script should configure the host to allow traffic to NGINX. 
    a.	Config should persist on host restart.
3.	Write an NGINX configuration for a new virtual host. 
    a.	Should listen to port 3200.
    b.	Should proxy traffic from www.example.com and deliver it to a backend host named localhost on port 3400.
4.	Send all non www.example.com traffic to a custom 404 page.
5.	NGINX should start if the host is restarted.



Saltstack
A docker-ized Saltstack fleet, for use with training materials.

Add the number of Salt minions desired in docker-compose.yml (add a new object for each new node), then save and deploy:

$ docker-compose up -d                                                                            
Creating network "saltstack_default" with the default driver
Creating saltstack_salt-master_1
Creating saltstack_salt-minion-3_1
Creating saltstack_salt-minion-2_1
Creating saltstack_salt-minion-1_1
After allowing some time for the minions to connect to the master, and the script to accept their keys, you can access the fleet:

$ docker exec saltstack_salt-master_1 salt "*" test.ping                                          
salt-minion-lonely_kalam:
    True
salt-minion-sick_goodall:
    True
salt-minion-cocky_kirch:
    True
