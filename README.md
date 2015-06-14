# Puppet Demo

Simple demo of Puppet. 
This demo uses Vagrant in order to setup a ready to use development environment.

# Author
* Matteo Galli - mondora.com

# Try it!

## Requirements

Install Vagrant for your system: https://www.vagrantup.com/

## Start Vagrant Machine

* git clone https://github.com/matteogll/puppet-demo.git`
* Start the virtual machine by using `vagrant up` command (from the project root)
* SSH into the VM: `vagrant ssh`
* The shared folder of the guest OS is: `/vagrant`

# List of demos
## Demo1
Use Puppet to install and customize Nginx.

* `vagrant ssh`: enter into the guest OS
* get root privileges: `sudo su`
* puppet apply -v -e "include demo1"`
* go to http://localhost:7080

# Note

Vagrantfile will make a symbolic link to `/vagrant/modules` in order to override default Puppet modules directory 
`/etc/puppet/modules`.