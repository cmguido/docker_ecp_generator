# Magento Docker Test Site Generator
------
**This is NOT meant for production purposes!!**
This was developed on a MacBook but it should work with all OS as long as you have docker and docker compose installed.  Please report any issues you face and I'll take a look as soon as I can.

-------

### What does it do?
This installs the last version of Magento 1.9 (1.9.3.8 to be exact).  This is the last Magento 1.x release that oracle released before deprecating support for Magento 1.

### How do I monitor the app created?
I personally use docker desktop but you can use portainer or any other docker monitoring system you want!

### Start Magento 1.9
Click on the "create" button below to create the app containers.  

You then want to run the command below in your terminal to get the magento container id to install sample data
`docker container ls` 
Find the one that says "alexcheng/magento" and use that for the next two commands.  

Install sample data by running the below two commands in the terminal with the container id from the previous command
`docker exec -it <container-id> install-sampledata` 
and
`docker exec -it <container-id> install-magento`
**Sample data must be installed before Magento**

### Useful info
**Admin Panel:** 127.0.0.1/admin

**Admin User:** admin

**Admin Pass:** magentorocks1