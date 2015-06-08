# PUPPET DEMO VAGRANTFILE

# Startup scripts
$script = <<SCRIPT
apt-get update
# Install Apache and PHP modules
apt-get install -y git nano puppetmaster puppet
rm -r /etc/puppet/modules/
ln -s /vagrant/modules /etc/puppet/modules
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
# BRIDGED NETWORK: config.vm.network "public_network"
# NAT NETWORK:
  config.vm.network "forwarded_port", guest: 80, host: 7080
  config.vm.provision "shell", inline: $script
end
