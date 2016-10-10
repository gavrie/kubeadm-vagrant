# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.box_check_update = false

  config.vm.provision :shell, :path => "install.sh"

  config.hostmanager.enabled = true
  config.hostmanager.manage_guest = true

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.77.10"

  # config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = "1024"
  end

  config.vm.define "n1" do |c|
      c.vm.hostname = "n1"
      c.vm.network "private_network", ip: "192.168.77.10"
  end

  config.vm.define "n2" do |c|
      c.vm.hostname = "n2"
      c.vm.network "private_network", ip: "192.168.77.11"
  end

  config.vm.define "n3" do |c|
      c.vm.hostname = "n3"
      c.vm.network "private_network", ip: "192.168.77.12"
  end

end
