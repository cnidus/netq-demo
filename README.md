# netq-demo
Deploy the Cumulus NetQ packages

# Introduction
This project deploys the Cumulus NetQ feature to a demo topology based on Cumulus VX. NetQ is a command-line troubleshooting tool for viewing various information from any switch or management device. It also allows for viewing state at a time in the past. More info on Cumulus NetQ can be found in Cumulus Documentation: https://docs.cumulusnetworks.com/display/DOCS/Using+netq+to+Troubleshoot+the+Network

The project has the following dependancies.

cldemo-vagrant - https://github.com/CumulusNetworks/cldemo-vagrant
cldemo-automation-ansible - https://github.com/CumulusNetworks/cldemo-automation-ansible

# Installing the demo
Firstly, you will need to install VirtualBox and Vagrant, to support the cldemo-vagrant reference topology shown above. That project has good documentation on gettign the base envrionment up.

Next, follow the procedure in cldemo-automation-ansible to provision the 2-spine, 2-leaf, 2-server environment.

Once you have provisioned and run base configuration, get to the oob-mgmt-server.

Dougs-MBP:cldemo-vagrant doug$ vagrant ssh oob-mgmt-server
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 4.2.0-27-generic x86_64)

 * Documentation:  https://help.ubuntu.com/
----------------------------------------------------------------
  Ubuntu 14.04.4 LTS                          built 2016-06-06
----------------------------------------------------------------
Last login: Wed Sep 14 20:34:34 2016 from 10.0.2.2
vagrant@oob-mgmt-server:~$ su - cumulus
Password: 
cumulus@oob-mgmt-server:~$ 

Password is the defualt: "CumulusLinux!"

Clone the repo into the cumulus home directory, get into that directory::
cumulus@oob-mgmt-server:~$ git clone https://github.com/cnidus/netq-demo.git
cumulus@oob-mgmt-server:~$ cd netq-demo

.... to be continue, once I have it working.d

