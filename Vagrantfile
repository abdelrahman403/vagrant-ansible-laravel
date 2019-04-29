
Vagrant.configure("2") do |config|

	config.vm.box = "centos7_serv"
	config.ssh.password = "vagrant"
	#config.vm.network "public_network", bridge: 'wlp10s0', ip: '192.168.1.10'
	config.vm.network "forwarded_port", guest: 80, host: 8080
	#config.vm.synced_folder "../shared_data", "/vagrantdata",
	#:owner => 'vagrant',
    #	:group => 'apache',
    #	:mount_options => ['dmode=775', 'fmode=664']
	
	config.vm.provider "virtualbox" do |vb|
		vb.name = "backend_server_test"
	end
	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "laravel/site.yml"
	end

end
