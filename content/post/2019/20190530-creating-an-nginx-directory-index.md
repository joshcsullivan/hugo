---
title: "Creating an NGinx Directory Index for Image and File Hosting"
slug: creating-an-nginx-directory-index
date: 2019-05-30T11:03:00-04:00
draft: false
tags: ["digitalocean", "nginx"]
categories: ["Tech"]
---

Due to [Phil's][1] post on his wiki about [Self Hosting Images][2] I reached out to him how he had set it up and then realized I had already done something similar but forgot about it.

So without further explanation I'm listing out the steps I took to set up the NGinx Directory Index Listing.

On a DigitalOcean droplet (or any Ubuntu/Linux VPS) already set up with Nginx (if you need instructions for setting up NGinx Firewall access, follow steps 12-14 [here][3]), follow these steps:

1. Get a domain or subdomain for the new site. In this example I used static.domain.com
2. To restrict its access you can create a new folder in the home directory of your user profile (`mkdir public`), for example mine is `/home/username/public` 
3.  While SSH'd into the VPS, navigate to `/etc/nginx/sites-available/` then create `static.domain.com` by entering `sudo nano static.domain.com`
4.  In the File put the following (make sure to change the path in root to your path)

```
server {
        server_name static.domain.com;
        root /home/username/public;
        autoindex on;
        autoindex_exact_size off;
        autoindex_format html;
        autoindex_localtime on; 
}
```

- Change the `server_name` field to your domain name
- **Make sure to change the path in root to your path**

5. Next you need to enable the site via Symbolic link: `sudo ln -s /etc/nginx/sites-available/static.domain.com /etc/nginx/sites-enabled/ - Symbolic links site to enabled`
6. For an SSL Cert if you have cert bot install you can skip to step 9, otherwise continue to 7
7. Enter `sudo apt install certbot - Install Certbot`
8. Enter `sudo apt-get install python-certbot-nginx` - Installs Nginx Certbot
9. Enter `sudo certbot --nginx` - Create HTTPS cert with Let’s Encrypt
	- Select whichever domains you want your cert to cover
	- Press 2 to redirect HTTP traffic to HTTPS, this is recommended
	- The conf files for your selected domains will be updated with the cert information automatically

You should now be able to access your NGinx directory index at `static.domain.com` while any folders inside that directory will now be accessible at `static.domain.com/folder/`

Sources: 
- [Enabling the Nginx Directory Index Listing][4]

[1]: https://youneedastereo.com/
[2]: https://youneedastereo.com/#how%20I%20self-host%20images%20in%20this%20wiki
[3]: https://blog.joshsullivan.io/2019/02/20/creating-online-tiddlywiki
[4]: https://www.keycdn.com/support/nginx-directory-index