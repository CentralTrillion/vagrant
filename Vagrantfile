VAGRANTFILE_API_VERSION = "2"
Vagrant.require_version ">= 1.7.2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	config.vm.define "main", primary: true do |node|
		
		node.vm.box = "centraltrillion/docker"
		node.vm.box_version = ">= 1.0.0"

		node.vm.network "private_network", ip: "10.0.0.10"
		
		node.vm.network "forwarded_port", guest: 80, host: 8080

		node.vm.provider "virtualbox" do |vb|
			vb.customize ["modifyvm", :id, "--memory", "2048"]
		end

	end

end
