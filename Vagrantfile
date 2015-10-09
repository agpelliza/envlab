# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ARTACK/debian-jessie"
  config.vm.network :forwarded_port, host: 4567, guest: 80

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/setup.yml"
  end
end
