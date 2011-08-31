Vagrant::Config.run do |config|
  config.vm.box = "lucid64"
  config.vm.box_url = "http://files.vagrantup.com/lucid64.box"
  config.vm.network "33.33.33.10"

  config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = "cookbooks"
     chef.recipe_url = "https://github.com/crowdint/vagrant-setup/blob/master/downloads/cookbooks.tar.gz"

     chef.add_recipe "general"
     chef.add_recipe "general::utils"
     # chef.add_recipe "mongodb"
     # chef.add_recipe "mysql"
     # chef.add_recipe "postgresql"
     chef.add_recipe "redis"
     # chef.add_recipe "solr"
  end

  config.vm.customize do |vm|
    vm.memory_size = 1024
  end
end
