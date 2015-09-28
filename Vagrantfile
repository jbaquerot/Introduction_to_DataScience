# -*- mode: ruby -*-
# vi: set ft=ruby :

# VM configuration parameters
boxRam = 2048                      # Ram in MB
boxCpus = 1                        # Number of CPU core

ipythonPort = 8001                 # Ipython port to forward (also set in IPython notebook config)

Vagrant.configure(2) do |config|
  config.ssh.insert_key = true 

  
  config.vm.define "IntroDataScience" do |master|
    master.vm.box = "jbaquerot/IntroDataScience"
    master.vm.box_download_insecure = true
    master.vm.boot_timeout = 900
    master.vm.network :forwarded_port, host: ipythonPort, guest: ipythonPort, auto_correct: true   # IPython port (set in notebook config)
    master.vm.network :forwarded_port, host: 4040, guest: 4040, auto_correct: true                 # Spark UI (Driver)
    master.vm.hostname = "IntroDataScience"
    master.vm.usable_port_range = 4040..4090
    master.vm.provider :virtualbox do |v|
      v.name = master.vm.hostname.to_s
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
<<<<<<< HEAD
<<<<<<< Updated upstream
      v.customize ["modifyvm", :id, "--memory", "#{boxRam}"]
      v.customize ["modifyvm", :id, "--cpus", "#{boxCpus}"]
=======
>>>>>>> Stashed changes
    end

=======
      v.customize ["modifyvm", :id, "--memory", "#{boxRam}"]
      v.customize ["modifyvm", :id, "--cpus", "#{boxCpus}"]
    end
>>>>>>> origin/master
    master.vm.synced_folder "data/", "/home/vagrant/data"
    master.vm.synced_folder "notebooks/", "/home/vagrant/notebooks"
  end
  config.ssh.private_key_path = "./keys/private_key"

end
