# -*- coding: utf-8 -*-
$:.unshift("/Library/RubyMotion/lib")
require 'motion/project/template/ios'
# require 'bubble-wrap/core'

begin
  require 'bundler'
  Bundler.require
rescue LoadError
end

Motion::Project::App.setup do |app|
  # Use `rake config' to see complete project settings.
  app.name = 'ercode'
  app.seed_id = '3V9K57L9SW'
 app.deployment_target = '7.0'
  app.device_family = [:iphone, :ipad]
  # app.interface_orientations = [:portrait, :portrait_upside_down]
  app.identifier = 'de.i2dm.ercode'
  app.version = '1.0'
  app.short_version = '1.0.0'
  # app.icons = Dir.glob("resources/Icon*.png").map{|icon| icon.split("/").last}
  app.prerendered_icon = true
  app.info_plist['UIRequiredDeviceCapabilities'] = {'location-services' => true }
  app.entitlements['application-identifier'] = app.seed_id + '.' + app.identifier

  # app.vendor_project('vendor/PDColoredProgress', :static)
  
  app.frameworks += ['AVFoundation']

  app.development do
    app.provisioning_profile = '/Users/dong/Library/MobileDevice/Provisioning Profiles/363a58d2-5712-4e2e-a7dc-2e984ddd1a69.mobileprovision'
    app.codesign_certificate = 'Dong Wang (7Y59E87GCZ)'
  end
   
  app.release do
    # app.info_plist['AppStoreRelease'] = true
    app.provisioning_profile = '/Users/dong/Library/MobileDevice/Provisioning Profiles/F026DE6C-51B6-4586-915A-48C0FA467E41.mobileprovision'
    app.codesign_certificate = 'iPhone Distribution: i2dm consulting & development GmbH'
  end
end