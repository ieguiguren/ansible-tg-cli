Vagrant.configure("2") do |config|

  # Setup Debian Jessie 64
  config.vm.define "jessie", primary: true do |jessie|
    jessie.vm.box = "debian/jessie64"
    jessie.vm.synced_folder ".", "/vagrant", disabled: true
  end
  
  # Setup Debian Wheezy 64
  config.vm.define "wheezy", autostart:false do |wheezy|
    wheezy.vm.box = "debian/wheezy64"
  end
  
  # Setup Ubuntu Trusty 64 14.04 Box.
  config.vm.define "trusty", autostart:false do |trusty|
    trusty.vm.box = "ubuntu/trusty64"
  end

  # Setup Ubuntu Precise 64 12.04 Box.
  config.vm.define "precise", autostart:false do |precise|
    precise.vm.box = "ubuntu/precise64"
  end

  # Setup CentOS 7
  config.vm.define "centos", autostart:false do |centos|
    centos.vm.box = "centos/7"
  end


  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "2048"
  end

  config.ssh.insert_key = false

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "vvvv"
    ansible.playbook = "tests/test.yml"
  end
end


