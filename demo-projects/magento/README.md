# Magento Docker Test Site Generator
------
**This is NOT meant for production purposes!!**
This should work with all OS as long as you have docker and docker compose installed.  Please report any issues you face and I'll take a look as soon as I can.

-------

### What does it do?
This installs the last version of Magento 1.9 (1.9.3.8 to be exact).  This is the last Magento 1.9 release that oracle released before deprecating support for Magento 1.

### How do I monitor the app created?
I personally use docker desktop but you can use portainer or any other docker monitoring tool you want!

### Start Magento 1.9
Click on the "up" button below to create the app containers.  

You then want to run the command below in your terminal to get the magento container id to install sample data and start the SSH service
`docker container ls` 
Find the one that says "alexcheng/magento" and use that for the next two commands.  

Install sample data and set up the magento instance by running the below command (unix)
`docker exec -it <container-id> /usr/local/bin/install-all`

OR (windows)
`docker exec -it <container-id> bash -c "dos2unix /usr/local/bin/install-all;/usr/local/bin/install-all;"`

If you want to start ssh service, run the command below
**You will need to run this each time you start the container to enable ssh access**
`echo -e "root\nroot" | docker exec -i <container-id> passwd && docker exec -it <container-id> service ssh restart`


### Useful info
**Magento Admin Panel:** 127.0.0.1/admin

**Magento Admin User:** admin

**Magento Admin Pass:** magentorocks1

**SSH Admin User:** root

**SSH Admin Pass:** root