# -*- mode: ruby -*-
# vi: set ft=ruby :

# リファレンス 
# https://docs.vagrantup.com.
Vagrant.configure("2") do |config|

  config.vm.box = "centos7.2"
  config.vm.network "private_network", ip: "192.168.33.60"

  config.vm.define :sample do |sample|
    sample.vm.hostname = 'sample'
    # ゲスト側にansibleをインストール
    config.vm.provision 'ansible_local' do |ansible|
      ansible.playbook = './sample.yml'
    end
  end
end
