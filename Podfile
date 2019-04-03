# Uncomment the next line to define a global platform for your project
 platform :ios, '9.0'

target 'TestPod' do
  # Uncomment the next line if you're using Swift or would like to use dynamic frameworks
  # use_frameworks!

  # Pods for TestPod

pod 'download', :path => './TestPod/LocalLib/download/'

####################加入代码##################
#post_install do |installer|
#  installer.pods_project.targets.each do |target|
#    target.build_configurations.each do |config|
#      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] ='8.0'
#      config.build_settings['ENABLE_BITCODE'] = 'YES'
#    end
#  end
#end
###遍历每个develop target，将target支持版本统一设成一个支持ARC的版本。
####################加入代码##################

### 实现post_install Hooks
#post_install do |installer|
#   # 1. 遍历项目中所有target
#   installer.pods_project.targets.each do |target|
#      # 2. 遍历build_configurations
#      target.build_configurations.each do |config|
#         # 3.1 修改build_settings中的ENABLE_BITCODE
#         config.build_settings['ENABLE_BITCODE'] = 'YES'
#          #3.2遍历每个develop target，将target支持版本统一设成一个支持ARC的版本。
#         config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] ='8.0'
#        end
#   end
#end

#### post_install start ####
post_install do |installer|
  # puts 为在终端打印方法
  puts "#### post_install start ####"
  
  # 为了打印的日志方便查看，使用╟符号修饰
  puts "╟ installer"
  # 获取属性名称列表，并遍历
  installer.instance_variables.each do |variableName|
    # 打印属性名称
    puts "╟ #{variableName}"
  end
  
  puts "╟ installer.public_methods"
  # 获取方法名称列表，并遍历
  installer.public_methods.each do |method|
    # 打印方法名称
    puts " ╟#{method}"
  end
  
  # 为了打印的日志方便查看，使用╟符号修饰
  puts "╟ podfile"
  # 打印podfile属性列表
  installer.podfile.instance_variables.each do |variableName|
    # 遍历属性并打印
    puts "  ╟ #{variableName}"
  end
  
  puts "╟ lockfile"
  # 打印lockfile属性列表
  installer.lockfile.instance_variables.each do |variableName|
    # 遍历属性并打印
    puts "  ╟ #{variableName}"
  end
  
  puts "##### post_install end #####"
end

  target 'TestPodTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'TestPodUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end
