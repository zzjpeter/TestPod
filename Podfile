# Uncomment the next line to define a global platform for your project
 platform :ios, '9.0'

target 'TestPod' do
  # Uncomment the next line if you're using Swift or would like to use dynamic frameworks
  # use_frameworks!

  # Pods for TestPod

pod 'download', :path => './TestPod/LocalLib/download/'

##################加入代码##################
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] ='8.0'
    end
  end
end
##################加入代码##################

  target 'TestPodTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'TestPodUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end
