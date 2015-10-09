# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "shell", run: "always", inline: <<-SHELL
sudo apt-get update
sudo apt-get install -y libssl-dev libpam-dev bundler
cd /vagrant && bundle && ./script/cibuild
SHELL
end
