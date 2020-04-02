# -*- mode: ruby -*-
# vi: set ft=ruby :

BOX_IMAGE = "hashicorp/precise64"
NAMES = ['master', 'worker']

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  NAMES.each do |name|
    config.vm.define "#{name}" do |subconfig|
      subconfig.vm.box = BOX_IMAGE
    end
  end

end
