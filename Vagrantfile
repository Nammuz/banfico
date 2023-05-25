Vagrant.configure("2") do |config|
  # Configure the provider
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "256"
    vb.cpus = 1
  end

  # Provision the first CentOS instance
  config.vm.define "haproxy1" do |node|
    node.vm.box = "generic/centos7"
    node.vm.hostname = "haproxy1"
    node.vm.network "private_network", ip: "192.168.0.92"

    node.vm.provision "shell", inline: <<-SHELL
      # Update system packages
      sudo yum -y update
    SHELL
  end

  config.vm.define "haproxy2" do |node|
    node.vm.box = "generic/centos7"
    node.vm.hostname = "haproxy2"
    node.vm.network "private_network", ip: "192.168.0.93"

    node.vm.provision "shell", inline: <<-SHELL
      # Update system packages
      sudo yum -y update
    SHELL
  end
end

