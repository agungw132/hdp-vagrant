# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "bento/centos-7.4"

  # Fixes changes from https://github.com/mitchellh/vagrant/pull/4707
  config.ssh.insert_key = false

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.

  # CentOS 7.0 x86_64
  #config.vm.box_url = "http://cloud.terry.im/vagrant/oraclelinux-7-x86_64.box"

  # HARDWARE NOTE: Change this values according to your hardware.
  config.vm.define :c7401 do |c7401|
    c7401.vm.hostname = "c7401.hdp.testlab"
    c7401.vm.network :private_network, ip: "192.168.74.201"
    c7401.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "16000"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7401.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7402 do |c7402|
    c7402.vm.hostname = "c7402.hdp.testlab"
    c7402.vm.network :private_network, ip: "192.168.74.202"
    c7402.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end    
    c7402.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7403 do |c7403|
    c7403.vm.hostname = "c7403.hdp.testlab"
    c7403.vm.network :private_network, ip: "192.168.74.203"
    c7403.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]    
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7403.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7404 do |c7404|
    c7404.vm.hostname = "c7404.hdp.testlab"
    c7404.vm.network :private_network, ip: "192.168.74.204"
    c7404.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7404.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7405 do |c7405|
    c7405.vm.hostname = "c7405.hdp.testlab"
    c7405.vm.network :private_network, ip: "192.168.74.205"
    c7405.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]    
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7405.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7406 do |c7406|
    c7406.vm.hostname = "c7406.hdp.testlab"
    c7406.vm.network :private_network, ip: "192.168.74.206"
    c7406.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7406.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7407 do |c7407|
    c7407.vm.hostname = "c7407.hdp.testlab"
    c7407.vm.network :private_network, ip: "192.168.74.207"
    c7407.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7407.vm.provision :shell, :path => "bootstrap.sh"
  end

  config.vm.define :c7408 do |c7408|
    c7408.vm.hostname = "c7408.hdp.testlab"
    c7408.vm.network :private_network, ip: "192.168.74.208"
    c7408.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7408.vm.provision :shell, :path => "bootstrap.sh"
  end
  
  config.vm.define :c7409 do |c7409|
    c7409.vm.hostname = "c7409.hdp.testlab"
    c7409.vm.network :private_network, ip: "192.168.74.209"
    c7409.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7409.vm.provision :shell, :path => "bootstrap.sh"
  end  

  config.vm.define :c7410 do |c7410|
    c7410.vm.hostname = "c7410.hdp.testlab"
    c7410.vm.network :private_network, ip: "192.168.74.210"
    c7410.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "4096"]
      vb.customize ["modifyvm", :id, "--cpus", "4"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", 90] # Single virtual CPU can use up to 90% of a single host CPU.
    end
    c7410.vm.provision :shell, :path => "bootstrap.sh"
  end 
end
