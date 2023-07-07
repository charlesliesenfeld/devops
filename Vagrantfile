
Vagrant.configure("2") do |config|

 config.vm.box = "centos/7"

 config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
 config.vm.provision "shell", path: "provision.sh", run: 'always'
 config.vbguest.auto_update = false 
 config.vm.synced_folder ".", "/vagrant", type: "rsync", rsync__exclude: ".git/"

end
