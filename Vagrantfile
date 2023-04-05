# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/centos-7.9"
  config.vm.box_check_update = true
 # config.vm.box_url = "https://github.com/CommanderK5/packer-centos-template/releases/download/0.7.2/vagrant-centos-7.2.box"
  config.ssh.insert_key = false
  config.vm.network "private_network", ip: "192.168.33.10"
  #config.vm.network :forwarded_port, guest: 8000, host: 8000
  config.vm.synced_folder "..", "/bahmni", :owner => "vagrant"
  config.vm.provider "virtualbox" do |vb|
  vb.customize ["modifyvm", :id, "--memory", 3092, "--cpus", 2 ,"--name", "sjt_dev"]

  end
end
