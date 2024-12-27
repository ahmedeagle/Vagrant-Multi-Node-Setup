Vagrant.configure("2") do |config|
  # Node 1
  config.vm.define "node1" do |node1|
    node1.vm.box = "ubuntu/bionic64" # Small Linux VM
    node1.vm.network "private_network", ip: "192.168.56.101"
    node1.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = 1
    end
  end

  # Node 2
  config.vm.define "node2" do |node2|
    node2.vm.box = "ubuntu/bionic64"
    node2.vm.network "private_network", ip: "192.168.56.102"
    node2.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = 1
    end
  end

  # Node 3
  config.vm.define "node3" do |node3|
    node3.vm.box = "ubuntu/bionic64"
    node3.vm.network "private_network", ip: "192.168.56.103"
    node3.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.cpus = 1
    end
  end
end
