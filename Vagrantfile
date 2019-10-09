# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.define :proxy do |n|
    n.vm.box = "ubuntu/bionic64"

    n.vm.network :private_network, ip: '192.168.99.21'

    n.vm.provision :ansible do |ansible|
      ansible.playbook = 'proxy.yml'
    end
  end

  config.vm.define :jenkins do |n|
    n.vm.network :private_network, ip: '192.168.99.22'

    n.vm.provision :ansible do |ansible|
      ansible.playbook = 'jenkins.yml'
    end
  end

  config.vm.define :echo do |n|
    n.vm.network :private_network, ip: '192.168.99.23'

    n.vm.provision :ansible do |ansible|
      ansible.playbook = 'echo.yml'
    end
  end
end
