
Vagrant.configure('2') do |config|
  config.vm.define 'ansible-role-common' do |c|
    c.vm.box = 'ubuntu/xenial64'
    c.vm.network :private_network, ip: '192.168.88.10'
    c.vm.hostname = 'common.local'
    c.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      ansible.host_key_checking = false
      ansible.limit = 'all'
    end
  end
end
