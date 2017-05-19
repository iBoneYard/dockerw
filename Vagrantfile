# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder "./scripts", "/home/ubuntu/scripts"
  config.vm.synced_folder "./SampleApp", "/home/ubuntu/SampleApp"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "docker-demo"
    vb.gui = false
    vb.memory = 1024
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get -y dist-upgrade
    apt-get -y autoremove
    apt-get clean
  SHELL
end
