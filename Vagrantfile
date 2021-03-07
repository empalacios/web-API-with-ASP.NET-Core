# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/contrib-buster64"

  config.vm.network "private_network", ip: "192.168.56.4"
  config.vm.network "forwarded_port",  guest: 5000, host: 5000

  config.vm.provision "shell", inline: <<-SHELL
    adduser vagrant adm
    
    apt-get update

    # NuGet
      apt-get install -y nuget
      nuget update -self

    # DotNet Core 5.0
    # Installation information: https://docs.microsoft.com/es-es/dotnet/core/install/linux-debian
      wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
      dpkg -i packages-microsoft-prod.deb
      apt-get update
      apt-get install -y apt-transport-https \
        && apt-get update \
        && apt-get install -y dotnet-sdk-5.0
  SHELL
end

