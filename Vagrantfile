# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "raring64"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/raring/current/raring-server-cloudimg-amd64-vagrant-disk1.box"
  #config.vm.box = "wheezy-7.2.0"
  #config.vm.box_url = "https://dl.dropboxusercontent.com/u/197673519/debian-7.2.0.box"
  config.ssh.forward_agent = true

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provision/drupal-single.yml"
    #ansible.inventory_path = "provision/inventories/ansible_hosts"
    ansible.sudo = true
    ansible.verbose = 'v'
  end
end
