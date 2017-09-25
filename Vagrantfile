Vagrant.configure("2") do |config|
  config.vm.box = "debian/jessie64"
  config.vm.hostname = "sonarqube.box"
  config.vm.provision "docker"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1792
    v.cpus = 2
  end

  config.vm.provision :docker_compose, yml: "/vagrant/docker-compose.yml", run: "always"

  config.vm.network "forwarded_port", guest: 9000, host: 9000
  config.vm.network "forwarded_port", guest: 9092, host: 9092

  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 50000, host: 50000
end
