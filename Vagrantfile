Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = "1024"
    v.cpus = 2
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"]
  end

  config.vm.define "cdbc01" do |cdbc01|
#   cdbc01.vm.box = "bento/centos-6.7"
    cdbc01.vm.box = "bento/centos-7.3"
    cdbc01.vm.hostname = "cdbc01"
    #cdbc01.vm.box = "wharton-wcit/centos6py36"
    cdbc01.vm.network "private_network", ip: "192.168.60.50"
    cdbc01.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbc01.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbc01.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbc01.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbc01.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.define "cdbcHA01" do |cdbcHA01|
#   cdbcHA01.vm.box = "bento/centos-6.7"
    cdbcHA01.vm.box = "bento/centos-7.3"
    cdbcHA01.vm.hostname = "cdbc01"
    #cdbcHA01.vm.box = "wharton-wcit/centos6py36"
    cdbcHA01.vm.network "private_network", ip: "192.168.60.150"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.define "cdbw01" do |cdbw01|
#   cdbw01.vm.box = "bento/centos-6.7"
    cdbw01.vm.box = "bento/centos-7.3"
    cdbw01.vm.hostname = "cdbw01"
    #cdbw01.vm.box = "wharton-wcit/centos6py36"
    cdbw01.vm.network "private_network", ip: "192.168.60.55"
    cdbw01.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbw01.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbw01.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbw01.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbw01.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.define "cdbw02" do |cdbw02|
#   cdbw02.vm.box = "bento/centos-6.7"
    cdbw02.vm.box = "bento/centos-7.3"
    cdbw02.vm.hostname = "cdbw02"
    #cdbw02.vm.box = "wharton-wcit/centos6py36"
    cdbw02.vm.network "private_network", ip: "192.168.60.56"
    cdbw02.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbw02.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbw02.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbw02.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbw02.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.define "cdbw03" do |cdbw03|
#   cdbw03.vm.box = "bento/centos-6.7"
    cdbw03.vm.box = "bento/centos-7.3"
    cdbw03.vm.hostname = "cdbw03"
    #cdbw02.vm.box = "wharton-wcit/centos6py36"
    cdbw03.vm.network "private_network", ip: "192.168.60.57"
    cdbw03.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbw03.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbw03.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbw03.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbw03.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.define "cdbtest" do |cdbtest|
#   cdbtest.vm.box = "bento/centos-6.7"
    cdbtest.vm.box = "bento/centos-7.3"
    cdbtest.vm.hostname = "cdbtest"
    #cdbc01.vm.box = "wharton-wcit/centos6py36"
    cdbtest.vm.network "private_network", ip: "192.168.60.60"
    cdbtest.vm.provision "shell", :inline => "sudo echo '192.168.60.50 cdbc01.local cdbc01' >> /etc/hosts"
    cdbtest.vm.provision "shell", :inline => "sudo echo '192.168.60.55 cdbw01.local cdbw01' >> /etc/hosts"
    cdbtest.vm.provision "shell", :inline => "sudo echo '192.168.60.56 cdbw02.local cdbw02' >> /etc/hosts"
    cdbtest.vm.provision "shell", :inline => "sudo echo '192.168.60.57 cdbw03.local cdbw03' >> /etc/hosts"
    cdbtest.vm.provision "shell", :inline => "sudo echo '192.168.60.60 cdbtest.local cdbtest' >> /etc/hosts"
    cdbcHA01.vm.provision "shell", :inline => "sudo echo '192.168.60.150 cdbc01.local cdbcHA01' >> /etc/hosts"

  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "citus_singlesetup.yml"
    ansible.inventory_path = "vagrant_hosts"
  end
  #config.vm.provision "ansible" do |ansible|
    #ansible.playbook = "citus_singlesetup.yml"
    #ansible.inventory_path = "vagrant_hosts"
    #ansible.tags = ansible_tags
    #ansible.extra_vars = ansible_extra_vars
    #ansible.limit = ansible_limit
  #end

end
