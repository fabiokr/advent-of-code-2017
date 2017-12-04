# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.define "elixir_box" do |elixir_box|
    elixir_box.vm.provider "virtualbox" do |v|
      v.name = "advent-of-code-elixir"
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 2]
    end
    elixir_box.vm.provision :shell, :path => "vagrant_provision.sh"
  end

  config.vm.synced_folder ".", "/home/vagrant/advent-of-code-2017"
end
