# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
  config.vm.box = "debian/buster64"
  config.vm.box_check_update = true
  config.vm.hostname = "oficemag"  
  config.vm.network "public_network", ip: "192.168.1.100"
  config.vm.define "oficemag"
  config.vm.provider "virtualbox" do |vb|
     vb.gui = false
     vb.memory = "2048"
	 vb.cpus = 2
	 vb.disksize.size = '10GB'
  end
  config.vm.provision "rep", type: "shell", inline: "echo сейчас что то будет...; apt-get install apt-transport-https lsb-release ca-certificates; wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg;echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list;"
  config.vm.provision "update", type: "shell", inline: "echo установка обновлений, не выключайте компьютер; apt-get update"
  config.vm.provision "vim", type: "shell", inline: "echo сейчас как поставим vim; apt-get install -y vim"
  config.vm.provision "wget", type: "shell", inline: "echo сейчас как поставим wget; apt-get install -y wget"
  config.vm.provision "htop", type: "shell", inline: "echo сейчас как поставим htop; apt-get install -y htop"
  config.vm.provision "tmux", type: "shell", inline: "echo сейчас как поставим tmux; apt-get install -y tmux"
  config.vm.provision "php5.6", type: "shell", inline: "echo сейчас как поставим php5.6; apt-get install -y php5.6"
  config.vm.provision "nginx", type: "shell", inline: "echo сейчас как поставим nginx; apt-get install -y nginx"
  config.vm.provision "apache2", type: "shell", inline: "echo сейчас как поставим apache2; apt-get install -y apache2"
  end
end
