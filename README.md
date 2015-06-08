# Puppet Demo

Simple demo of Puppet. 
This demo uses Vagrant in order to setup a ready to use development environment.

# Author
* Matteo Galli - mondora.com

# Try it!

## Preconditions

Install Vagrant for your system: https://www.vagrantup.com/

## Start Vagrant Machine

* Start the virtual machine by using `vagrant up` command (from the project root)
* SSH into the VM: `vagrant ssh`
* The shared folder is: `/vagrant`

# List of demos
## Demo1
Use Puppet to install and customize Nginx.

* vagrant ssh
* puppet apply -v -e "include demo1"
* go to http://localhost:7080

# Note

Vagrantfile will make a symbolic link to `/vagrant/modules` in order to override default Puppet modules directory 
`/etc/puppet/modules`.