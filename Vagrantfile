# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
	config.vm.box = 'ubuntu/bionic64'

	config.vm.network 'forwarded_port', guest: 3000, host: 3000
	config.vm.hostname = 'sisop'
	config.vm.provider 'virtualbox' do |vb|
		vb.memory = '2048'
		vb.name = config.vm.hostname
	end

	config.vm.provision 'shell', privileged: false, inline: <<-SHELL
		sudo apt-get update
		sudo apt-get install -y git make gdb qemu-system-x86 python3-dev
		sudo apt-get install -y seabios libbsd-dev gcc-multilib libc6-dev linux-libc-dev
		sudo cp /vagrant/cp-jos /usr/local/bin
	SHELL
end

