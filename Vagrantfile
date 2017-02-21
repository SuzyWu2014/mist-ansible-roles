Vagrant.configure(2) do |config|
  # config.vm.box = "puphpet/debian75-x64"
  config.vm.box_url = "https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box"
  config.vm.box = "centos-6.7"
  config.vm.define "servers"
  config.vm.network "private_network", ip: "192.168.33.14"
  config.ssh.username = "vagrant" # default password: vagrant
  config.ssh.insert_key = false
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "example-main.yml"
    # ansible.host_vars = {
    #   "servers" => {"http_port" => 9200,}
    # }
  end
end