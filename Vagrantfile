# -*- mode: ruby -*-
# vi: set ft=ruby :
 
# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
 
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
 
  # This is kinda ghetto, but the simplest way to print a message to the user
  puts "\nNOTE: After the box boots, your app will be available at e.g. http://192.168.50.1:8080"
  puts "      If Vagrant won't detect the machine state, just Ctrl + C after the GUI is up\n\n"
 
  config.vm.box = "Svpernova09/Windows7-php7dev"
 
  # Makes the host machine available as "192.168.50.1" on the guest
  config.vm.network "private_network", ip: "192.168.50.2"
 
  # http://stackoverflow.com/questions/23574387/why-is-vagrant-trying-to-ssh-to-windows-guest
  # https://www.vagrantup.com/blog/feature-preview-vagrant-1-6-windows.html
  config.vm.communicator = "winrm"
 
  # We don't want the default headless mode
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
  end
end

