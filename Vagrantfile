# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/precise64"
  config.vm.box_url   = 'http://files.vagrantup.com/precise64.box'


  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  config.vm.network :forwarded_port, host: 3000, guest: 3000

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "ansible/playbook.yml"
    #ansible.verbose = "v"
  end
end
