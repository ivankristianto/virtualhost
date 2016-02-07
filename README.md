Virtualhost Manage Script
===========

Bash Script to allow create or delete apache virtual hosts on Centos 7 on a quick way.
Modified from https://github.com/RoverWire/virtualhost

## Installation ##

1. Download the script
1. Create sites-enabled and sites-available directory
        $ mkdir /etc/httpd/sites-available
        $ mkdir /etc/httpd/sites-enabled

1. Apply permission to execute:

        $ chmod +x /path/to/virtualhost.sh

1. Optional: if you want to use the script globally, then you need to copy the file to your /usr/local/bin directory, is better
if you copy it without the .sh extension:

        $ sudo cp /path/to/virtualhost.sh /usr/local/bin/virtualhost

### For Global Shortcut ###

        $ cd /usr/local/bin
        $ wget -O virtualhost https://raw.githubusercontent.com/ivankristianto/virtualhost/master/virtualhost.sh
        $ chmod +x virtualhost

## Usage ##

Basic command line syntax:

    $ sudo sh /path/to/virtualhost.sh [create | delete] [domain] [optional host_dir]

With script installed on /usr/local/bin

    $ sudo virtualhost [create | delete] [domain] [optional host_dir]


### Examples ###

to create a new virtual host:

    $ sudo virtualhost create mysite.dev

to create a new virtual host with custom directory name:

    $ sudo virtualhost create anothersite.dev my_dir

to delete a virtual host

    $ sudo virtualhost delete mysite.dev

to delete a virtual host with custom directory name:

    $ sudo virtualhost delete anothersite.dev my_dir