# What is this repo?
This is my own project, a service where I customize the egg for you. This is free of charge, so I can't commit my time 24/7 but I try to at least respond quickly and get out status updates to you.
### I haven't been consistent at all
Yes, I know this; I plan to continue with this, I just kind of forgot about it. This is something I'm doing as part of Sigma Productions, but this is not a service we offer as a group; that's why it is under my personal Github account.

# Pterodactyl webhost egg

How to use:
1. Go to releases and download the json file
2. Import the egg to your panel like you normally do
3. Create a new server, additionally you can enable wordpress, this will install wordpress for you
and you can also install composer packages, this can also be done after the install
4. Navigate to the given port and ip and you are good to go just add you files to the webroot folder
(when using wordpress go to http://ip:port/wp-admin)
Note: if you want it using a domain then create a reverse proxy on the host 


To remove logs from console, open nginx/conf.d/default.conf and uncomment (remove #):

```
#access_log /home/container/naccess.log;
#error_log  /home/container/nerror.log error
```


Originally forked and edited from https://gitlab.com/tenten8401/pterodactyl-nginx


© Sigma Productions 2024
