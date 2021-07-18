# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    # Every Vagrant development environment requires a box. You can search for
    # boxes at https://vagrantcloud.com/search.
    config.vm.box = "hashicorp/bionic64"

    # Create a private network, which allows host-only access to the machine
    # using a specific IP.
    config.vm.network "private_network", ip: "192.168.87.10"

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "4096"
        vb.cpus = 2
    end

    #
    config.vm.provision "tools", type: "ansible_local" do |ansible|
        ansible.playbook = "ansible/tools/playbook.yaml"
    end

end
