# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Alfresco!"
  config.vm.define "alfresco" do |app_config|
    app_config.vm.box = "CentosAlfresco"
    app_config.vm.box_url = "http://inzynieria.it/CentosAlfresco.box"
    app_config.vm.network :private_network, ip: "192.168.11.11"
    app_config.vm.provider :virtualbox do |vb|  
      vb.customize ["modifyvm", :id, "--memory", "2024", "--cpus", "2", "--ioapic", "on"]
    end
  end
end

