# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Debian test box
  #config.vm.box = "puphpet/debian75-x64"
  config.vm.box = "thoomi/debian8-amd64"
  # Centos test box
  #config.vm.box = "puppetlabs/centos-7.0-64-puppet"

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = true

  config.vm.define 'mailcatcher-dev' do |dev|
    dev.vm.hostname = 'mailcatcher.local'
    dev.vm.network :private_network, ip: '192.168.56.61'
    dev.vm.provision "ansible" do |ansible|
      ansible.groups     = {
        "dev"          => ["mailcatcher-dev"],
      }
      ansible.playbook   = "provisioning/playbook.yml"
    end
  end
end

