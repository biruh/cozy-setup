# Cozy Setup

Cozy Setup contains all stuff needed to install cozy on a fresh debian server.

# How To Install Cozy Environnement

The installation requires system up to date with upstart as daemon manager.

You can do it with following commands.

> guest$ sudo apt-get update  
> guest$ sudo apt-get upgrade  
> guest$ sudo apt-get install upstart  
> guest$ sudo reboot now  

Then use the Fabric script to launch the cozy install

> host$ fab -H user@ip:port install

Fill what you want when installer will ask you information about the
certificate. 

Be patient some commands or app deployements could take few minutes. It depends about your network and your hardware capabilities.

# Test 

If nothing goes wrong, you can access to https://IP:80 to create your cozy
main account.

The port 80 must be open on the (virtual) machine. 

For Vagrant user, uncomment this line in the Vagrantfile and reload the vm.

> config.vm.network :hostonly, "192.168.33.10"

> vagrant reload


# Issues on 20 june.

The Postfix (mail server) configuration is set to mycozycloud.com . 
Right now Cozy has just mail sending capabilities. So you don't need a perfect
configuration. Mails are only required to notify you what to do when you need
to reset your password.

Redis is set to default conf.



# About Cozy

Cozy is private pesronal cloud solution that allows you to host all your 
personnal application in a single place you control. 
This way, you can manage your data efficiently while protecting your privacy.

http://www.mycozycloud.com
