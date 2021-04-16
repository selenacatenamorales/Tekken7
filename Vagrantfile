# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "tekkenweb"
  config.vm.define "tekkenweb"
  config.vm.network "private_network", ip: "192.168.52.73"
  config.vm.network "forwarded_port", guest: 3306, host: 1234
  config.vm.provision "shell", path: "script.sh"
  config.vm.synced_folder "html/", "/var/www/html"
  config.vm.provider "virtualbox" do |vb|
	vb.name = "tekkenweb"
    vb.memory = "512"
    vb.cpus = 1
  end
end


