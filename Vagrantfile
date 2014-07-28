# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Common
  config.vm.provision :puppet do |puppet|
    puppet.module_path = "../djingo-modules"
    puppet.manifests_path  = "../djingo-manifests"
    puppet.manifest_file  = "site.pp"
    puppet.facter = {
      "vagrant" => "1"
    }
    puppet.options = "--pluginsync"
  end

  # kaspar.djingo.org
  config.vm.define "kaspar.djingo.org" do |kaspar|
    kaspar.vm.hostname = "kaspar.djingo.org"
    kaspar.vm.box = "trusty-server-cloudimg-amd64"
    kaspar.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    #kaspar.vm.network :forwarded_port, guest: 8140, host: 8140
  end

  # nepomuk.djingo.org
  config.vm.define "nepomuk.djingo.org" do |nepomuk|
    nepomuk.vm.hostname = "nepomuk.djingo.org"
    nepomuk.vm.box = "trusty-server-cloudimg-amd64"
    nepomuk.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    #nepomuk.vm.network :forwarded_port, guest: 8140, host: 8140
  end

  # nautilus.djingo.org
  config.vm.define "nautilus.djingo.org" do |nautilus|
    nautilus.vm.hostname = "nautilus.djingo.org"
    nautilus.vm.box = "trusty-server-cloudimg-amd64"
    nautilus.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    #nautilus.vm.network :forwarded_port, guest: 8140, host: 8140
  end

  #config.hiera.config_path = 'hiera'
  #config.hiera.config_file = 'hiera.yaml'
  #config.hiera.data_path   = 'hiera/hieradata'

end
