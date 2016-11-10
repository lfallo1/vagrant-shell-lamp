# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_ROOT = File.expand_path("..", Dir.pwd)

Vagrant.configure("2") do |config|

  config.vm.box = "centos-7.0"

  config.vm.network "forwarded_port", guest: 80, host: 9000

  config.vbguest.auto_update = false

  config.vm.provision "file", source: VAGRANT_ROOT + "\\provision\\files\\git-config", destination: "~/.config"
  config.vm.provision "shell", path: "https://raw.githubusercontent.com/lfallo1/vagrant-lamp/master/scripts/centos-lamp.sh"
end
