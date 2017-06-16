# This spins up a vagrant box running ubuntu 64 bit and forwards the ip traffic to localhost
Vagrant.configure("2") do |config|
  config.vm.hostname = "rob-vagrant-box"
  config.vm.box = "hashicorp/ubuntu64"
  # config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.network :forwarded_port, guest: 80, host: 4567, host_ip: "127.0.0.1"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end
end



