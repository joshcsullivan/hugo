---
title: "Creating an Online TiddlyWiki on DigitalOcean"
date: 2019-02-20T15:14:55-04:00
tags: ["wiki", "digitalocean", "nginx"]
categories: []
---

[TiddlyWiki][1] is a Wiki software that you can run a few different ways including locally only, online, or syncing a local wiki to an online wiki. You can see examples of online TiddlyWiki's here:
- [My Wiki][2]
- [Jack Baty's Wiki][3]
- [Phil Nunnally's Wiki][4]
- [h0p3's Wiki][5]
- [sphygm.us][6]

The following tutorial will be an explanation on how to create a TiddlyWiki on a DigitalOcean droplet.

## Initial Setup

1. Sign into [DigitalOcean][7] or create an account then create a Ubuntu 18.04 Droplet, the $5 tier is more than enough to start.
	 
2. Follow these instructions for initial server setup: [Initial Server Setup with Ubuntu 18.04][8]
3. On your domain provider, create the following Host Records:

|Type|Host|Value|
|---|---|---|
|A Record|@|IP Address of Droplet|
|A Record|www|IP Address of Droplet|

## Install NodeJS and NPM

All of the following are commands you can copy and paste once connected via SSH:

4. `sudo apt update` - Update the package index
	 
5. `sudo apt install nodejs npm` - Install NodeJS and NPM

6. `nodejs --version` - Check NodeJS version

7. `npm --version` - Check NPM version

## Install TiddlyWiki, Forever, and Nginx

8. `sudo npm install -g tiddlywiki` - Install TiddlyWiki

9. `sudo npm install -g forever` - Install Forever which allows you to continuously run TiddlyWiki without being connected via terminal

10. `sudo apt install nginx` - Install Nginx

11. `sudo ufw app list` - Get Firewall Available Applications

12. `sudo ufw allow 'Nginx HTTP'` - Allow Nginx HTTP traffic through the firewall

13. `sudo ufw allow 'Nginx HTTPS'` - Allow Nginx HTTPS traffic through the firewall

14. `systemctl status nginx` - Confirm Nginx is running the output should look like this:
	```
	? nginx.service - A high performance web server and a reverse proxy server
   Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
   Active: active (running) since Wed 2019-02-20 18:53:51 UTC; 1min 2s ago
	 Docs: man:nginx(8)
  Process: 8300 ExecStart=/usr/sbin/nginx -g daemon on; master\_process on; (code=exited, status=0/SUCCESS)
  Process: 8291 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master\_process on; (code=exited, status=0/SUCCESS)
 Main PID: 8304 (nginx)
	Tasks: 2 (limit: 1152)
   CGroup: /system.slice/nginx.service
	       +-8304 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;
	       +-8306 nginx: worker process
	```

## Initialize TiddlyWiki

15. `mkdir -p ~/apps/wiki` - Make a folder in your home folder called `apps` with a sub folder `wiki` (you can name this whatever you would like)

16. `cd apps/wiki` - Open the new folder

17. `tiddlywiki mywiki --init server` - Create a new wiki in `mywiki` folder, you can change that name to what you would like.

## Initialize Nginx and Add SSL via Certbot from Let's Encrypt
18. `cd /etc/nginx/sites-available/` - CD into Nginx directory

19. `sudo nano /etc/nginx/sites-available/DOMAIN.com` This will create your domain config file

20. Paste the following into the file and change `DOMAIN.com` and `www.DOMAIN.com` to your domain:

```
server {
	server_name DOMAIN.com www.DOMAIN.com;
	
	location / {
	proxy_pass   http://127.0.0.1:8080;
	proxy_set_header        Host             $host;
	proxy_set_header        X-Real-IP        $remote_addr;
	proxy_set_header        X-Forwarded-For  $proxy_add_x_forwarded_for;
	}
}
```

Press **Ctrl+O** then Enter then **Ctrl+X** to save the file then exit the file

21. `sudo ln -s /etc/nginx/sites-available/DOMAIN.com /etc/nginx/sites-enabled/` - Symbolic links site to enabled

22. `sudo apt install certbot` - Install Certbot

23. `sudo apt-get install python-certbot-nginx` Install Nginx Certbot plugin

24. `sudo certbot --nginx` - Create HTTPS cert with Let's Encrypt
	- Select whichever domains you want your cert to cover
	- Press 2 to redirect HTTP traffic to HTTPS, this is recommended
	- The conf files for your selected domains will be updated with the cert information automatically

## Running TiddlyWiki
25. `cd ~/PATH/TO/WIKIFOLDER` Do not go into the directory of the wiki just to the folder that contains your wiki folder, for example if you created the directory as listed in step 14: `cd ~/apps/wiki/`

26. `tiddlywiki mywiki --listen` replacing mywiki to what your wiki folder is called
	- Now navigate to your domain in a web browser and it should be served correctly.

27. To run the process without being connected to the server:
		`forever start --spinSleepTime 10000 /usr/local/bin/tiddlywiki /home/username/apps/wiki/mywiki --listen "readers=(anon)" writers=USERNAME username=USERNAME password=PASSWORD`

28. Alternatively you can create a CSV file add it to the root of mywiki and run the following command which will allow anyone to read your wiki but only authenticated via the CSV to write:
	`forever start --spinSleepTime 10000 /usr/local/bin/tiddlywiki /home/username/apps/wiki/mywiki --listen credentials=users.csv "readers=(anon)" "writers=(authenticated)"`

29. For Restricted reading and writing:
	`forever start --spinSleepTime 10000 /usr/local/bin/tiddlywiki /home/username/apps/wiki/mywiki --listen credentials=users.csv "readers=(authenticated)" "writers=(authenticated)"`

## Conclusion
I've been using TiddlyWiki since Friday, February 15, 2019, and have fallen in love with it. It gives me the flexibility I need for keeping track of all kinds of data and doesn't make you stick to a rigid structure. Tiddlers (entries) are not required to connect to another, and therefore you can have Orphan Tiddlers that are only called upon by linking to one.

I highly recommend at least downloading TiddlyWiki to your local computer and trying it out if you are looking for a wiki software or something similar. Also, check out the Wikis I've listed above to see if there are new use cases you might not have thought of yet. 

Finally, if TiddlyWiki isn't for you, there is always [DokuWiki][9] as an alternative. An excellent example of DokuWiki is [Andrew Canion's Wiki][10], have a look there to see if that fits better with your style.

Please feel free to reach out to me with any questions or comments via [Micro.blog][11] or via email: contact {AT} sullivantss.com

[1]:	https://tiddlywiki.com/
[2]:	https://joshisms.io
[3]:	https://rudimentarylathe.org/
[4]:	https://twelvety.com/tiddlywiki.html
[5]:	https://philosopher.life/
[6]:	https://sphygm.us/
[7]:	https://www.digitalocean.com/
[8]:	https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04
[9]:	https://www.dokuwiki.org/dokuwiki
[10]:	https://andrewcanion.com/wiki/doku.php?
[11]:	https://micro.blog/joshsullivan