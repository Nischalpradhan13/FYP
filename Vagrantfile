Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box_download_insecure = true    
    master.vm.box = "centos/7"
    master.vm.network "private_network", ip: "192.168.56.105"
    master.vm.hostname = "master"
    master.vm.provider "virtualbox" do |v|
      v.name = "master"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "worker" do |worker|
    worker.vm.box_download_insecure = true 
    worker.vm.box = "centos/7"
    worker.vm.network "private_network", ip: "192.168.56.106"
    worker.vm.hostname = "worker"
    worker.vm.provider "virtualbox" do |v|
      v.name = "worker"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "rancher" do |rancher|
    rancher.vm.box_download_insecure = true
    rancher.vm.box = "centos/7"
    rancher.vm.network "private_network", ip: "192.168.56.107"
    rancher.vm.network "forwarded_port", guest: 80, host: 84
    rancher.vm.network "forwarded_port", guest: 443, host: 7443
    rancher.vm.hostname = "rancher"
    rancher.vm.provider "virtualbox" do |v|
      v.name = "rancher"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm. define "zabbix" do |zabbix|
    zabbix.vm.box_download_insecure = true
    zabbix.vm.box = "centos/7"                                                 
    zabbix.vm.network "private_network", ip: "192.168.56.108"
    zabbix.vm.hostname = "zabbix"
    zabbix.vm.provider "virtualbox" do |v|
      v.name = "zabbix"
      v.memory = 4096
      v.cpus = 2
    end
 end

end
