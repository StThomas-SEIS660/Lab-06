#Lab 06

In this lab, you will assemble into your teams and install the open source monitoring tool Nagios in a client-server configuration.

## Configuring X windows

We will spend some time as a class determining whether and how X-windows is working for you all.

## Getting started

Four pairs of virtual machines have been created:

manos01, nervios01
manos02, nervios02
manos03, nervios03
manos04, nervios04

The goal is to

* install the Nagios server on your nervios instance
* install the Nagios agent on your manos instance
* configure Nagios to monitor your manos instance
* test that it is working by halting manos and observing the result
* further test by bringing manos back up and observing the result

## Steps

First, log into the nervios instance appropriate to your team.

You should log in with the following options:

    ssh -XC -c blowfish-cbc,arcfour  yourID@seis660.gps.stthomas.edu

The extra options are so that X-windows performs better (they make a big difference!)

The instructions we will follow this time are at:

http://www.unixmen.com/install-configure-nagios-4-ubuntu-14-1014-04/

At this point, you should have the command line skills to install and configure nagios based on these directions, which will not be repeated here.

Towards the end of the directions, you will log into manosXX (again the instance appropriate to your team) and configure it so that it can be monitored by the nagios server.

You will then make a final configuration file change on nervios and restart nagios. If you have followed the instructions correctly, it should start monitoring your manos instance.

You can log in and see your nagios instance by opening a new ssh session and typing

    firefox -X -no-remote

Test that your monitoring is working correctly by issuing the command

    vagrant halt manosXX

replacing the XX as appropriate for your team.

In 5 minutes, you should see an error on the web portal. Restart your manos server:

    vagrant up manosXX

and observe the result on your web portal. 
