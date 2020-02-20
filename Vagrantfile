# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|

config.vm.provision "shell", inline: <<-SHELL

        sudo apt-get update

   SHELL


config.vm.define "box1" do |box1|


    box1.vm.box="ubuntu/trusty64"

    box1.vm.network :forwarded_port, guest: 22, host: 10212, id: "ssh"

    box1.vm.network :private_network, ip: "192.167.56.101"

    box1.vm.provider :virtualbox do |v|

    v.customize ["modifyvm", :id, "--memory", 1020]

#       virtualbox_intnet: true  

      end

end

#You need to add missing keyword 'end'- see below.  Comment by Svetlana Gluhova on 2-20-2020

end
