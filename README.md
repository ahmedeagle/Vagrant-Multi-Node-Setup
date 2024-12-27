
Vagrant Multi-Node Setup
This repository contains a Vagrant configuration to create and manage multiple virtual machines (VMs) for development or testing purposes. The setup is based on ubuntu/bionic64 boxes with private networking.

Features
Creates three nodes (node1, node2, node3).
Assigns private IPs for each node.
Configurable resources (CPU, memory) for each VM.
Uses VirtualBox as the default provider.
Prerequisites
Vagrant (version 2.2+ recommended)
VirtualBox (version 6+ recommended)
Getting Started
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/vagrant-multi-node-setup.git
cd vagrant-multi-node-setup
2. Update the Vagrantfile (Optional)
Edit the Vagrantfile to customize:

IP addresses
CPU and memory allocation
3. Start the VMs
To bring up all VMs:

bash
Copy code
vagrant up
To bring up a specific node:

bash
Copy code
vagrant up node1
4. Check VM Status
bash
Copy code
vagrant status
5. SSH into a Node
bash
Copy code
vagrant ssh node1
Node Configuration
The Vagrantfile defines the following nodes:

Node 1
IP: 192.168.56.101
Memory: 512 MB
CPUs: 1
Node 2
IP: 192.168.56.102
Memory: 512 MB
CPUs: 1
Node 3
IP: 192.168.56.103
Memory: 512 MB
CPUs: 1
Adding More Nodes
To add more nodes, edit the Vagrantfile and define additional nodes using the same structure. Example:

ruby
Copy code
config.vm.define "node4" do |node4|
  node4.vm.box = "ubuntu/bionic64"
  node4.vm.network "private_network", ip: "192.168.56.104"
  node4.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    vb.cpus = 1
  end
end
Then start the new node:

bash
Copy code
vagrant up node4
Stopping and Destroying Nodes
Stop all nodes:
bash
Copy code
vagrant halt
Stop a specific node:
bash
Copy code
vagrant halt node1
Destroy all nodes:
bash
Copy code
vagrant destroy
Destroy a specific node:
bash
Copy code
vagrant destroy node1
License
