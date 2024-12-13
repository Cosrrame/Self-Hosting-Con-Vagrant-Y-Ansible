# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"

  config.vm.define "mrm" do |mrm|
    mrm.vm.network "private_network", ip: "192.168.57.10"

    # Provisión con Ansible
    mrm.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "provision.yml"
    end
  end
end
