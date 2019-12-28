---
title: vagrantfile
created: '2019-12-25T10:59:18.542Z'
modified: '2019-12-25T11:26:26.727Z'
---

# vagrantfile

## example
```ruby
Vagrant.configure(2) do |config|
	config.vm.box = "chef/centos-6.5"         # Specifying the box we wish to use
	config.vm.network "public_network"        # Adding Bridged Network Adapter

	(1..3).each do |i|                              # Iterating the loop for three times
		config.vm.define "edureka_vm#{i}" do |node|   # Defining VM properties
			config.vm.provider "virtualbox" do |node|   # Specifying the provider as VirtualBox and naming the VM's	
				node.name = "edureka_vm#{i}"              # The VM will be named as edureka_vm{i}
			end
		end
	end

end
```

## see also
- [[vagrant]]
