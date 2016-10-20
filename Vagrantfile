# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/centos7"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provision "shell", inline: <<-SHELL
    yum update -y
    yum -y group install "Development Tools"
    timedatectl set-timezone Asia/Tokyo
    localectl set-locale LANG=ja_JP.UTF-8
    curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -
    yum -y install nodejs
    npm install -g typescript
    npm install -g gulp-cli
  SHELL
end
