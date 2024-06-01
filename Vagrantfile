# Vagrantfile

Vagrant.configure("2") do |config|
  # Specify the box you want to use
  config.vm.box = "ubuntu/bionic64" # You can use any other box as per your requirement

  # Forward the port 5001 from guest to host
  config.vm.network :forwarded_port, guest: 5001, host: 5001

  # You can add more configurations as needed
  # For example, setting up a private network
  # config.vm.network "private_network", type: "dhcp"

  # Provisioning: Install required packages and dependencies
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y python3-lxml
    sudo pip3 install flask_cors
    sudo pip3 install flasgger
    # Additional provisioning steps
  SHELL
end
