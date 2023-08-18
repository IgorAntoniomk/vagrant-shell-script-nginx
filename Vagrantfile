																																			
Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"

  config.vm.provider "virtualbox" do |v|
    v.name = "vagrant-shell-script-nginx"
  end

config.vm.box_download_insecure=true

config.vm.network "forwarded_port", guest: 80, host: 8090

config.vm.network "public_network"

config.vm.provision "shell", path: "script.sh" 

config.vm.synced_folder "site/", "/var/www/html"
  
end
