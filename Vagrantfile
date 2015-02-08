# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
echo Cloning Repo...
git clone https://github.com/ishowcase/iWantThis ~/tmp/iWantThis

echo Moving to working dir...
cp -rf ~/tmp/iWantThis/* /vagrant/

echo Installing dependancies...
cd /vagrant/
bower install

echo Script completed successfully.
SCRIPT


Vagrant.configure("2") do |config|

  config.vm.box = "scotch/box"
  config.vm.network "private_network", ip: "192.168.33.10"
#  config.vm.network "forwarded_port", guest: 80, host: 3080
  config.vm.hostname = "scotchbox"
  config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
  config.vm.provision "shell",
    inline: $script,
    privileged: false
end