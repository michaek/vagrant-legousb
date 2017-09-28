# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.10"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--usb", "on"]
    vb.customize ["modifyvm", :id, "--usbehci", "on"]
    vb.customize ["usbfilter", "add", "0",
      "--target", :id,
      "--name", "LEGO USB Tower",
      "--manufacturer", "LEGO Group",
      "--product", "LEGO USB Tower"]
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get install -y nqc
  SHELL
end
