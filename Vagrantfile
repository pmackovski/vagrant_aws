Vagrant.configure("2") do |config|
  config.vm.box = "proserv-au"

  config.vm.provider :aws do |aws, override|

      # Ubuntu Server 14.04 LTS (HVM), SSD Volume Type
      aws.ami = "ami-ba3e14d9"
      aws.keypair_name = "phil"
      aws.security_groups = "vagrant"
      aws.instance_type = "t2.micro"
      aws.tags = {'Owner' => 'Vagrant'}

      override.ssh.username = "ubuntu"
      override.ssh.private_key_path = "~/phil.pem"
  end
end
