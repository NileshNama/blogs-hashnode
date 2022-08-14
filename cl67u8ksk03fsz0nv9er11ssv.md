## How to put a website Online  ?

# 1. Domain Registration:
- first you need to buy a domain name `Example:  nileshnama.com` for your website from google domains/ go daddy /Namecheap / .tech domains or any other domain registrar. 

Now
-  the question is where are  the our website stay or live actually  ?? where we have to put all html css and other files?

so for that we need to store it somewhere . but where ?

it can be our computer as well but the problem is that our website need to be upto-date and alive 24/7. 
& we have to manually set & mantain security and others essential stuff to stay it online.

so better way to handle it by use others computers known as servers specifically web servers. 
now next step is to host(store) our website.

# 2. Hosting
Now we need a place where our website can  live.

there are tons of hosting providers that they give us `shared server/virtual  private server/ dedicated servers` of thier server computers that are located on the data centers across the world.

i would like to grab your attention at very crucial thing, there are generally 2 types of hosting provider out there. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660446435175/_BzHOK3Ox.png align="left")

1. managed hosting(shared) provider: --
all the security and and other essential stuff will be handle by them, we need to no worry at all about it.
some are hostinger/ blue host/ siteground etc. best for blogers or bussiness persons.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660446547253/ZJ05dN4r2.png align="left")


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660446671998/v32kqD94x.png align="left")


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660446728796/-twQa6J3G.png align="left")

2. cloud hosting provider: --
provider just gives us a bare virtual system, all the thing we have to manage by ourself.
some are  digital ocean/ Linode/ aws/ google cloud etc. best for software developers who want to explore the server management.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660446833933/vgi7hVeVm.png align="left")

according your needs. must  to purchase any one hosting service.

- how to host your website on that purchased  server? , you can refer offical documents.

#  3. Connect Domain Name with hosting Server or Provider

to understand it very clearly,  i would explain how actually things happen when we search a domain in browser.

as soon as we type  nileshnama.com and hit enter
then your computer uses DNS to find Nameservers for nileshnama.com, 

 then the computer finds nileshnama.com's public nameservers
then computer ask for the A Record or address from name server, then the public name server will respond with the IP address of your server where the site exist.


so by this process we can understand some imp steps:

1.   we need to set the name servers of the hosting provider to our domain registrar. 
2.  `A ` record must be setup to get the IP Address of our server, apart from this we can set alias for our domain. popular alias for each website is WWW can save in `Cname` Record. there are other as well you can refer official documents.


DNS Setting will take 24-48 hrs to reflect changes.

Now the last but very important step,

# 4. Security
https://....... this is recomended by google itself so
Adding a SSL/TSL certification from either hosting provider or `lets encrypt` via certbot.

so congrats your website is live online now!


✨thats all from my side thank you. 













