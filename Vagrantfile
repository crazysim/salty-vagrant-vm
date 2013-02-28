# require "../lib/vagrant-salt"

Vagrant::Config.run do |config|
  ## Chose your base box
  config.vm.box = "opscode-ubuntu-12.04"
  config.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04_chef-11.2.0.box"

  ## For masterless, mount your salt file root
  config.vm.share_folder "salt_file_root", "/srv", "salt/roots/"


  ## Use all the defaults:
  config.vm.provision :salt do |salt|
    salt.run_highstate = false

    ## Optional Settings:
    # salt.minion_config = "salt/minion.conf"
    # salt.temp_config_dir = "/existing/folder/on/basebox/"
    # salt.salt_install_type = "git"
    # salt.salt_install_args = "develop"

    ## If you have a remote master setup, you can add
    ## your preseeded minion key
    # salt.minion_key = "salt/key/minion.pem"
    # salt.minion_pub = "salt/key/minion.pub"
  end
end
