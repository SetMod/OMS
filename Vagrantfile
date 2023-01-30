# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 4000, host: 4000, host_ip: "127.0.0.1"
  config.vm.synced_folder "./data", "/vagrant_data"

  config.vm.hostname = "oms"
  config.vm.define "oms"
  config.vm.provider "virtualbox" do |vb|
      vb.name = "oms"
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
  SHELL
end
