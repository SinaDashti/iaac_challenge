# -*- mode: ruby -*-
# vi: set ft=ruby :

BOX_IMAGE = "ubuntu/bionic64"
MACHINE = ["master","worker"]
N = 1

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  (0..N).each do |i|
    config.vm.define MACHINE[i] do |subconfig|
      subconfig.vm.box = BOX_IMAGE
      subconfig.vm.hostname = MACHINE[i]
      subconfig.vm.network :private_network, ip: "192.168.3.#{10+i}"
      # subconfig.vm.provision "ansible" do |ansible|
      #   ansible.playbook = "playbook.yml"
      # end
    end
  end

end
