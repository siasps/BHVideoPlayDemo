# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'VideoPlayDemo' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  # Pods for VideoPlayDemo

    pod 'FDFullscreenPopGesture'
    pod 'MJRefresh'
    pod 'ZFPlayer', '~> 4.0'
    pod 'ZFPlayer/ControlView', '~> 4.0'
    pod 'ZFPlayer/AVPlayer', '~> 4.0'    
    pod 'Masonry'

    #修复iOS14因为去掉arc相关过时文件，而引起的报错
    post_install do |installer|
      installer.generated_projects.each do |project|
        project.targets.each do |target|
          target.build_configurations.each do |config|
            config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '11.0'
            config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = "arm64"
          end
        end
      end
    end

end
