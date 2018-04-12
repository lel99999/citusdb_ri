Vagrant.configure("2") do |config|
  config.vm.define "cdbc01" do |cdbc01|
    cdbc01.vm.box = "bento/centos-6.7"
    cdbc01.vm.hostname = "cdbc01"
    #cdbc01.vm.box = "wharton-wcit/centos6py36"
    cdbc01.vm.network "private_network", ip: "192.168.60.150"
  end
  config.vm.define "cdbw01" do |cdbw01|
    cdbw01.vm.box = "bento/centos-6.7"
    cdbw01.vm.hostname = "cdbw01"
    #cdbw01.vm.box = "wharton-wcit/centos6py36"
    cdbw01.vm.network "private_network", ip: "192.168.60.155"
  end
  config.vm.define "cdbw02" do |cdbw02|
    cdbw02.vm.box = "bento/centos-6.7"
    cdbw02.vm.hostname = "cdbw02"
    #cdbw02.vm.box = "wharton-wcit/centos6py36"
    cdbw02.vm.network "private_network", ip: "192.168.60.156"
  end
  config.vm.define "cdbw03" do |cdbw03|
    cdbw03.vm.box = "bento/centos-6.7"
    cdbw03.vm.hostname = "cdbw03"
    #cdbw02.vm.box = "wharton-wcit/centos6py36"
    cdbw03.vm.network "private_network", ip: "192.168.60.157"
  end
  config.vm.define "cdbtest" do |cdbtest|
    cdbtest.vm.box = "bento/centos-6.7"
    cdbtest.vm.hostname = "cdbtest"
    #cdbc01.vm.box = "wharton-wcit/centos6py36"
    cdbtest.vm.network "private_network", ip: "192.168.60.160"
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
