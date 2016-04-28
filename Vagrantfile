# This guide is optimized for Vagrant 1.7 and above.
# Although versions 1.6.x should behave very similarly, it is recommended
# to upgrade instead of disabling the requirement below.
Vagrant.require_version ">= 1.7.0"

Vagrant.configure(2) do |config|
  config.vm.hostname = 'spark-experimental'
  config.vm.box = "ubuntu/trusty64"

  # zookeeper port
  # config.vm.network :forwarded_port, guest: 2181, host: 2181

  # Disable the new default behavior introduced in Vagrant 1.7, to
  # ensure that all Vagrant machines will use the same SSH key pair.
  # See https://github.com/mitchellh/vagrant/issues/5005
  config.ssh.insert_key = false

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "spark.yml"
  end

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end
end