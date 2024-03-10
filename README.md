#  Hack The Box Broker CTF New-Izi-Way
Here is a quick and easy way to get into the vm of the broker machine in Hack The Box CTF. 
I searched the internet but couldn't find a similar way so I thought I'd share it. 
The method is very easy as you can see in the pictures below.
Hitting the ip on the broswer,we see that it asks for credentials. I try the default admin/admin and boom we are in.
![Screenshot from 2024-03-10 14-10-22](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/d3d63e04-adf9-470e-865f-8cb6cba9f232)
The next part is to scan open doors on the machine with the command sudo nmap -Pn -T4 -v -p- -oN 10.10.11.221
![Screenshot from 2024-03-10 14-11-03](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/cccad236-09df-43bc-bc6f-dee60e8e3836)
In the photo below you can see which doors are open and I'm trying one by one on the broswer
![Screenshot from 2024-03-10 14-11-26](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/6dd952b8-e285-4ef1-a60d-f24f1509d10f)

The door that seems to be useful is 3456/tcp which brings out directories that exist on linux machines  
if you explore the path http://10.10.11.243:3456/home/activemq/user.txt/ you see the user.txt flag 4e85*********************
and also if you go to http://10.10.11.243:3456/root/root.txt you also see the root flag bccf***************
![Screenshot from 2024-03-10 14-11-59](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/03ede83e-8725-4c39-aa1a-c60998b87668)

![311535665-d7029f8f-3275-4e8d-b2c2-ebdc03fe43c3](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/9f51dc44-ef74-4ca5-8056-3ba763cdcd48)
![311535666-c87cf4a0-8827-46b6-b851-1f7633656cfc](https://github.com/hello4r1end/HTB_Broker-CTF-New-Izi-Way/assets/60706453/e1632de8-f135-46f9-935c-4ab3f2dbf53a)
