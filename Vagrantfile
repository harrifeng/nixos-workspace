Vagrant.configure("2") do |config|

  hostname = File.basename(Dir.getwd)
  config.vm.define "#{hostname}" do |app|
    app.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "4096"
      vb.cpus = 2
    end
    app.vm.hostname = "#{hostname}"
    app.vm.box = "nixos/nixos-18.03-x86_64"
    app.vm.box_check_update = false
    app.ssh.insert_key = false
    app.ssh.private_key_path = ['~/.vagrant.d/insecure_private_key']
    app.vm.network "private_network", ip: "10.19.19.22"
  end
end
