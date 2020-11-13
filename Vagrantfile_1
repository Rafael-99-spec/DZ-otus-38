# -*- mode: ruby -*-
# vim: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/8"
  config.vm.box_check_update = true

  
  config.vm.define "web", primary: true do |web|
    web.vm.hostname = 'web'
    web.vm.network "private_network", ip: "192.168.100.20"
	web.vm.provider :virtualbox do |w|
		w.name = "web"
		w.customize ["modifyvm", :id, "--cpus", 4, "--memory", "1024"]

    end

	web.vm.provision "ansible" do |ansible|
        ansible.playbook = "web.yml"
	end
	
  end


  
end
