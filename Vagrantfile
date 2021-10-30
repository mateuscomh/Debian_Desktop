
Vagrant.configure("2") do |config|

  config.vm.box = "debian/bullseye64"
  config.vm.network "forwarded_port", guest:22, host:2222
  config.vm.provider "virtualbox" do |v|
    v.cpus = 1
    v.memory = 1024
  end

  config.vm.define "deb" do |deb|
    deb.vm.network "private_network", ip: "172.17.177.41"
    deb.vm.network "forwarded_port", guest:22, host:2221
  end
  
  config.vm.provider "virtualbox" do |deb|
    deb.cpus = 2
    deb.memory = 1480
    deb.name = "debian_ansible"
  end

end
