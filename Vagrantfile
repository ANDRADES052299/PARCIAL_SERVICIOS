$script = <<-SCRIPT
echo I am provisioning...
sudo service firewalld stop
SCRIPT

Vagrant.configure("2") do |config|
	config.vm.define :clienteFw do |clienteFw|
		clienteFw.vm.box = "bento/centos-7.9"
		clienteFw.vm.network :public_network, ip: "192.168.100.18"
		clienteFw.vm.hostname = "clienteFw"
	end
	config.vm.define :firewall do |firewall|
		firewall.vm.box = "bento/centos-7.9"
		firewall.vm.network :public_network, ip: "192.168.100.20"
		firewall.vm.hostname = "firewall"
	end
	config.vm.define :servidor2 do |servidor2|
		servidor2.vm.box = "bento/centos-7.9"
		servidor2.vm.network :public_network, ip: "192.168.100.22"
		servidor2.vm.hostname = "servidor2"
	end
end
