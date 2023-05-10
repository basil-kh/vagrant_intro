
$script = <<-SCRIPT
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install nginx -y
sudo systemctl start nginx
sudo systemctl status nginx
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip:"192.168.10.100"
  config.vm.provision "shell", inline: $script
end
