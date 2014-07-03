Vagrant.require_version ">= 1.6.0"

VAGRANT_API_VERSION = '2'

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  config.vm.define "openconext" do |openconext|
    openconext.vm.network :private_network, ip: "192.168.111.100"
    openconext.vm.provision :ansible do |ansible|
      ansible.playbook = "openconext.yml"
      ansible.inventory_path = "inventory/development"
      ansible.verbose = "v"
    end
  end
end