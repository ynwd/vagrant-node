Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provision "shell", inline: <<-SHELL
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
    source ~/.nvm/nvm.sh
    echo "source ~/.nvm/nvm.sh && cd /vagrant" > ~/.bashrc
    nvm install --lts &> /dev/null
    nvm alias default stable
    node --version
  SHELL
end
