

# -*- mode: ruby -*-
# vi: set ft=ruby :
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.
  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
#Jenkins-box configuration
  config.vm.define "test_box" do |test_box|
    test_box.vm.box = "centos/7"
    test_box.vm.network "private_network", ip: "192.168.33.8"
    test_box.vm.network "public_network", bridge: "Intel(R) 82579LM Gigabit Network Connection"
    #test_box.ssh.username = "vagrant"
    #test_box.ssh.password = "vagrant"
    config.vm.provider "virtualbox" do |test_box|
      test_box.memory = 1048
      test_box.cpus = 1
    end
    config.vm.provision "shell", inline: <<-SHELL
       yum update all
       yum install -y python
     SHELL
  end
end`
