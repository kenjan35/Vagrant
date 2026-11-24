Vagrant.configure("2") do |config|

  config.vm.define "Server" do |server|
    server.vm.box = "cloudsoe/debian-13"
    server.vm.box_url = "https://boxes.cloudsoe.com/cloudsoe/debian-13.json"
    server.vm.hostname = "atolojan"

    server.vm.network "private_network", ip: "192.168.56.110"
    server.vm.provider "virtualbox" do |vb|
      vb.memory = 512
      vb.cpus = 1
    end
  end

end
