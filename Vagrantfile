# Runs the role against Ubuntu 14.04, 16.04 and CentOS 7
# for local testing purposes

Vagrant.configure("2") do |config|
  config.vm.define "centos7" do |centos7|
    centos7.vm.box = "centos/7"
    centos7.vm.hostname = "sec-ansible-test-centos-7"

    centos7.vm.provision "ansible" do |ansible|
      # ansible.verbose = "vvv"
      ansible.playbook = "tests/vagrant.yml"
      # we'll skip V-38496 because Vagrant itself creates the user that causes
      # this to fail
      ansible.skip_tags = ['V-38496']
      # we need to run as sudo for a lot of the checks ansible-security runs
      ansible.raw_arguments = ['-s']
    end
  end
end
