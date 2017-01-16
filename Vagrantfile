# -*- mode: ruby -*-
# vim: ft=ruby

# ---- Configuration Part -----
NAME = "nh"


# get IP - addition per defined user 
priv_ip = { "rk" => "0", 
			"sh" => "2", 
			"dawei" => "4", 
			"dk" => "6", 
			"nh" => "8"}

nodes = %w[ GENERALI
			SEEPEX
			PANASONIC
			InstILIAS
			TESTILIAS
		  ]

server = Array.new() { Array.new() }
nodes.each_with_index do |node, index|
	server.push( :hostname => "#{node}", :ip => "192.168.6." + priv_ip[NAME] + "#{index+2}" )
	puts "#{node} => #{index}"
end

puts server
# define the virtuel machines
# nodes = [
# 	{ :hostname => 'GENERALI', :ip => '192.168.6' + priv_ip[NAME] + '2'}.
# 	{ :hostname => 'SEEPEX', :ip => '192.168.6' + priv_ip[NAME] + '.3'},
# 	{ :hostname => 'PANASONIC', :ip => '192.168.6' + priv_ip[NAME] + '4'},
# 	{ :hostname => 'InstILIAS', :ip => '192.168.6' + priv_ip[NAME] + '5'}
# ]


# Vagrant.configure("2") do |config|
# 	config.vm.box = "debian/jessie64"

# 	# do for each virtual machine
# 	nodes.each do |node|
# 		config.vm.define node[:hostname] do |nodeconfig|
# 			puts node[:ip]
# 			nodeconfig.vm.hostname = node[:hostname]
# 			nodeconfig.vm.network :private_network, ip: node[:ip]
# 		end
# 	end

# 	config.vm.provision :ansible do |ansible|
# 		ansible.playbook = "playbook.yml"
# 		ansible.
# 		ansible.groups = { "webserver" => ["GENERALI", "SEEPEX", "PANASONIC", "InstILIAS"], "generali" => ["GENERALI"] }
# 	end
# end