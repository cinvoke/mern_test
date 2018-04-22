Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.synced_folder "./src", "/home/vagrant/src"

  config.vm.network :forwarded_port, guest: 4200, host: 4200

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "vv"
    ansible.playbook = "playbook.yml"
  end
end
