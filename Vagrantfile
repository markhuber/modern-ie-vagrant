# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_SERVER_URL'] ||= 'http://vagrant.markhuber.net/catalog'

boxes = [
  {:name => "IE10-Win7", :box => "dealertrack/IE10-Win7"},
  {:name => "IE10-Win8", :box => "dealertrack/IE10-Win8"},
  {:name => "IE11-Win10", :box => "dealertrack/IE11-Win10"},
  {:name => "IE11-Win7", :box => "dealertrack/IE11-Win7"},
  {:name => "IE11-Win8.1", :box => "dealertrack/IE11-Win8.1"},
  {:name => "IE6-WinXP", :box => "dealertrack/IE6-WinXP"},
  {:name => "IE7-Vista", :box => "dealertrack/IE7-Vista"},
  {:name => "IE8-Win7", :box => "dealertrack/IE8-Win7"},
  {:name => "IE8-WinXP", :box => "dealertrack/IE8-WinXP"},
  {:name => "IE9-Win7", :box => "dealertrack/IE9-Win7"}
]

Vagrant.configure(2) do |config|
  boxes.each do |box|
    config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    config.vm.define box[:name], autostart: false do |machine|
      machine.vm.box = box[:box]
    end
  end
end
