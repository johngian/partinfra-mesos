VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "512"]
  end

  # Mesos master1
  config.vm.define "master1" do |master|
    master.vm.hostname = "mesos-master1"
    master.vm.box = "ubuntu/trusty64"
    master.vm.network :private_network, ip: "192.168.60.4"
  end

  # Mesos master2
  config.vm.define "master2" do |master|
    master.vm.hostname = "mesos-master2"
    master.vm.box = "ubuntu/trusty64"
    master.vm.network :private_network, ip: "192.168.60.5"
  end

  # Mesos master2
  config.vm.define "master3" do |master|
    master.vm.hostname = "mesos-master3"
    master.vm.box = "ubuntu/trusty64"
    master.vm.network :private_network, ip: "192.168.60.6"
  end

  # Mesos slave1
  config.vm.define "slave1" do |slave|
    slave.vm.hostname = "mesos-slave1"
    slave.vm.box = "ubuntu/trusty64"
    slave.vm.network :private_network, ip: "192.168.60.7"
  end

  # Mesos slave2
  config.vm.define "slave2" do |slave|
    slave.vm.hostname = "mesos-slave2"
    slave.vm.box = "ubuntu/trusty64"
    slave.vm.network :private_network, ip: "192.168.60.8"
  end

  # Mesos slave3
  config.vm.define "slave3" do |slave|
    slave.vm.hostname = "mesos-slave3"
    slave.vm.box = "ubuntu/trusty64"
    slave.vm.network :private_network, ip: "192.168.60.9"
  end

end
