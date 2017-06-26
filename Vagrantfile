# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  # Configure VM Ram usage
  config.vm.provider :virtualbox do |p|
    p.customize ['modifyvm', :id, '--memory', '4096']
  end
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "https://atlas.hashicorp.com/ubuntu/boxes/trusty64"
  config.vm.network "forwarded_port", guest: 22, host: 2223, id: "ssh"
  config.vm.network "forwarded_port", guest: 3000, host: 3001
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.box_check_update = false
  config.vm.hostname   = "sports-personality"

end
