Vagrant.configure("2") do |config|
  config.vm.box = "debian-7.4.0-amd64"
  config.vm.box_url = "https://s3-eu-west-1.amazonaws.com/ffuenf-vagrant-boxes/debian/debian-7.4.0-amd64_virtualbox.box"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "512"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
  end

  config.vm.provision :ansible do |ansible|
    ansible.sudo = true
    ansible.host_key_checking = false
    ansible.playbook = "playbook.yml"
    ansible.verbose = "vv"
    #ansible.tags = ""
  end
end
