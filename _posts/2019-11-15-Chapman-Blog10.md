---
layout: post
title: "Blog 10"
---

Create a Certificate w/ Certbot
-------------------------------

1. SSH into the server running your website

2. Add the Certbot PPA with the following commands:

      $ sudo apt-get update
      $ sudo apt-get install software-properties-common
      $ sudo add-apt-repository universe
      $ sudo add-apt-repository ppa:certbot/certbot
      $ sudo apt-get update

3. Next, install Certbot with the following command:

      $ sudo apt-get install certbot

4. If you want to keep the web server running use:

      $ sudo certbot certonly --webroot

   If it's not running use:

      $ sudo certbot certonly --standalone

   If you need to different domains to be covered, enter the first domain [SPACE] the second domain.

5. Then install the new certificate in the web servers config file

6. Confirm the site is working by visiting the site online.
