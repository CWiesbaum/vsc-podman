Vagrant.configure("2") do |config|
  config.vm.box = "fedora/34-cloud-base"
  config.vm.box_version = "34.20210423.0"

  config.vm.provider "virtualbox" do |vbconfig|
    vbconfig.gui = false
    vbconfig.name = "podman_provider"
    vbconfig.memory = 16384
    vbconfig.cpus = 2
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end
end
