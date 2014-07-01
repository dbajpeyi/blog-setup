# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |devbox|

  # Every Vagrant virtual environment requires a box to build off of.
  devbox.vm.box = "precise64"
  devbox.vm.box_url = "http://files.vagrantup.com/precise64.box"

  devbox.vm.network :forwarded_port, guest: 80, host: 8002
  devbox.vm.network :private_network, ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # devbox.vm.network :public_network

  # If true, then any SSH connections made will enable agent forwarding.
  # Default value: false
  # devbox.ssh.forward_agent = true

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  devbox.vm.synced_folder ".", "/shared", disabled: true

  devbox.vm.hostname = "todo.dev"

  devbox.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/site.yml"
    ansible.inventory_path = "provision/hosts"
    ansible.limit = "local"
  end
end
