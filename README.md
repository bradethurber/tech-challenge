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
