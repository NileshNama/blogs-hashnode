## Server-Management

# setup droplet
- create a droplet (virtual private server) & Associate with it a project if needed.
- authentication of droplet with ssh is better than passwd method.


# login server as root
initially we can log in server as `root` via powershell/bash, type following command

```
ssh root@your_server_ip

``` 

```
sudo apt update
``` 

```
sudo apt upgrade
``` 


# Creating a non-root user

```
adduser Nilesh

``` 
now if you want to give root access to user 

```
usermod -aG sudo Nilesh
``` 

to access root previlages as `nonroot user`

```
sudo su
``` 

```
exit
``` 


# Firewall setup
first we need to give access to ur self 

```
ufw allow OpenSSH
``` 
Now we can turn on firewall 

```
ufw enable
``` 


```
sudo ufw status
``` 


```
ufw disable
``` 




---
# for website 

- first need to install a web server `nginx` or `apache`

```
sudo apt install apache2
``` 
OR

```
apt install nginx
``` 

- Make sure you allow ufw firewall permission  to nginx as well, check firewell section here.
for allow firewall web server

```
sudo ufw allow in "Apache Full/nginx full"
``` 


Now go to below directory 

```
cd /var/www/html/
``` 
in this directory we can find `index.html`. this is the web page show on this ip.

- for check cpu uilization run `sudo htop` command

---

Now ques is that how we can transfer files from local to our virtual private server??

# Filezilla
- enter hostname, ip , passwd & port 22.  after setup just drap & drop files.

# Enabling passwordless login to your server 

(for passwd less note that while generating ssh key, no passpharse add then only it can be passwd less)

- Step 1 - Create a private-public key pair in your `local system`


```
ssh-keygen -t rsa
``` 
This generates a private-public key pair on your computer. Press enter 3 times to choose the default options.

Step 2 - Deploy ssh key on your server 
so log in your server and make directory as follows as per user (if for user then make sure create this in `/home/nilesh`  directory)

```
cd ~
mkdir .ssh
``` 

This will create a .ssh in the home directory ('/home/Nilesh/' in my case) of your user. DigitalOcean droplet ships with a root account so creating this '.ssh' directory is not needed if you want to configure serverless login for root.

 so now go to your `local system`  & Execute the following command on your host(local) computer:


```
scp C:\Users\Nilesh\.ssh\id_rsa.pub Nilesh@ip-address:~/.ssh/authorized_keys
``` 
Step 3 - Test your passwordless login

```
ssh user@ip-address
``` 
---

# Quick login using Powershell profiles

Step 1 - Create a PowerShell profile
Create a PowerShell profile using the command below:

```
New-Item $profile -Type File -Force
``` 
This creates a PowerShell profile that will execute whenever you start PowerShell on your computer.

Step 2 - Open and add a function to the PowerShell profile
Open your PowerShell profile by executing the following command on Windows:

```
notepad $profile
``` 
As a part of the next step, we will add few functions to our PowerShell profile. Paste the following code to your profile


```
echo "Hello Nilesh, Welcome to PowerShell !" 

function personal{
    Start-Process ssh Nilesh@ip address
}

function client1{
    Start-Process ssh VG@thier-ip-address
}

function client2{
    Start-Process ssh iuVcare@ip-address
}
``` 
Replace the usernames and IP addresses with the actual values of your servers. Finally, save and close the file.

Step 3 - Test your profile
- need to restart PowerShell 
- and now just type client name & server will open without passwd, congrats

---
## Problem 1

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659385488846/yUpZFh6xM.png align="left")

Solution

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659385555229/AbsVT8zTR.png align="left")

---

# connect domain name with this droplet(server)
go to domain registrar (in our case- go to `google domains`) & select purchased domain name which you want to point this server.  and add the  record `A` and point the ip address of droplet. wait for 24-48hrs.

- other records also need to configure

## use record `CNAME` to  use alias tp point some other website or same website

```
www.nileshnama.com	CNAME	 nileshnama.com      1hour

``` 
above in this the `www` is alias to use same website that point nileshnama.com


```
blogs.nileshnama.com	CNAME	1 hour	   hashnode.network.

``` 
in above line the `blogs` is use as alias to point hashnode.network

- Create a wildcard DNS record
use `*` as alias and create `A` record and point this to ip address

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659413237132/XklP-NhIk.png align="left")


## How to enable HTTPs on Your Website ? 
Using Free Let’s Encrypt SSL/TLS Certificates with NGINX

1. Download the Let’s Encrypt Client
First, download the Let’s Encrypt client, certbot.
```
apt-get update
$ sudo apt-get install certbot
$ apt-get install python3-certbot-nginx
``` 

2. Set Up NGINX

- certbot can automatically configure NGINX for SSL/TLS. It looks for and modifies the server block in your NGINX configuration that contains a server_name directive with the domain name you’re requesting a certificate for. In our example, the domain is www.nileshnama.com.

- Assuming you’re starting with a fresh NGINX install, use a text editor to create a file in the /etc/nginx/conf.d directory named domain‑name.conf (so in our example, www.nileshnama.com.conf).

Specify your domain name (and variants, if any) with the server_name directive:


```
server {
    listen 80 default_server;
    listen [::]:80 default_server;
    root /var/www/html;
    server_name example.com www.example.com;
}
``` 
Save the file, then run this command to verify the syntax of your configuration and restart NGINX:

```
 nginx -t && nginx -s reload
``` 

3. Obtain the SSL/TLS Certificate

The NGINX plug‑in for certbot takes care of reconfiguring NGINX and reloading its configuration whenever necessary.

Run the following command to generate certificates with the NGINX plug‑in:

```
sudo certbot --nginx -d example.com -d www.example.com
``` 

- Note: Let’s Encrypt certificates expire after 90 days (on 2017-12-12 in the example). For information about automatically renenwing certificates, see Automatic Renewal of Let’s Encrypt Certificates below.

4. Automatically Renew Let’s Encrypt Certificates

Let’s Encrypt certificates expire after 90 days. We encourage you to renew your certificates automatically. Here we add a cron job to an existing crontab file to do this.
Open the crontab file.

```
crontab -e
``` 
Add the certbot command to run daily. In this example, we run the command every day at noon. The command checks to see if the certificate on the server will expire within the next 30 days, and renews it if so. The --quiet directive tells certbot not to generate output.

```
0 12 * * * /usr/bin/certbot renew --quiet
``` 
Save and close the file. All installed certificates will be automatically renewed and reloaded.

[free-ssltls-certificates-from-lets-encrypt-with-nginx](https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/)

---


## setup a virtual host  i.e. which directory or folder to use for website??  

- firstly make a new directory in `/var/www/` 

```
sudo mkdir -p /var/www/nileshnama.com/html
``` 
Now we have to give permission to user to edit files without sudo. here `nilesh_vps` is username

```
sudo chown -R $nilesh_vps:$nilesh_vps /var/www/nileshnama.com/html       
sudo chmod -R 755 /var/www         
``` 

Step 2 — Creating Sample Pages for Each Site
if we want to create files then we need sudo permision so

```
sudo vi index.html
``` 

OR  Transfer the site contents, Transfer the index.html and related files to the individual site directories using Filezilla.

Step 3 — Creating Server Block Files for Each Domain
As mentioned above, we will create our first server block config file by copying over the default file:

```
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/nileshnama.com
``` 
Now, open the new file you created in your text editor with sudo privileges:

```
sudo nano /etc/nginx/sites-available/example.com
``` 

Step 4 — Enabling your Server Blocks and Restart Nginx


```
sudo ln -s /etc/nginx/sites-available/nileshnama.com /etc/nginx/sites-enabled/
``` 

```
sudo nginx -t
``` 
[how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu by Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu-16-04)

Note :  check the default_server is set to only one host, nor for others

---
##  commands

to delete file or directory (remove (rm))
- rm filename
- rm -rf  dirName

---
✨ This is all from my side , Thank you !