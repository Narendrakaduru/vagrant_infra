Vagrant.configure("2") do |config|
  # Define variables with default values
  vm_name = ENV['VM_NAME'] || "Demo-Server"
  box_name = ENV['BOX_NAME'] || "bento/centos-7.9"
  private_ip = ENV['PRIVATE_IP'] || "192.168.10.100"
  hostname = ENV['HOSTNAME'] || "demo-server"
  memory_size = ENV['MEMORY_SIZE'] || 2048
  cpus = ENV['CPUS'] || 2

  # Configure Vagrant settings using variables
  config.vm.define vm_name
  config.vm.box = box_name
  config.vm.network "private_network", ip: private_ip
  config.vm.hostname = hostname

  config.vm.provider "virtualbox" do |vb|
    vb.name = vm_name
    vb.memory = memory_size
    vb.cpus = cpus
  end
end
