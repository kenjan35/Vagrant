Vagrant.configure("2") do |config|

  config.vm.define "atolojanS" do |server|
    server.vm.box = "cloudsoe/debian-13"
    server.vm.box_url = "https://boxes.cloudsoe.com/cloudsoe/debian-13.json"

    server.vm.network "private_network", ip: "192.168.56.110"
    server.vm.hostname = "atolojanS"
    server.vm.provider "virtualbox" do |vb|
      vb.memory = 512
      vb.cpus = 1
    end
  end

  config.vm.define "atolojanSW" do |agent|
    agent.vm.box = "cloudsoe/debian-13"
    agent.vm.box_url = "https://boxes.cloudsoe.com/cloudsoe/debian-13.json"

    agent.vm.network "private_network", ip: "192.168.56.111"
    agent.vm.hostname = "atolojanSW"
    agent.vm.provider "virtualbox" do |vb|
      vb.memory = 512
      vb.cpus = 1
    end
  end
end
