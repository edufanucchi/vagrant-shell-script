
Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vbox|
  vbox.name = "vagrant-shell-script"  
  vbox.memory = 2048
  vbox.cpus = 2
  end
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network"
  config.vm.synced_folder "site/", "/var/www/html"
  config.vm.provision "shell", path: "script.sh"

end
