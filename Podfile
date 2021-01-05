platform :ios, '12.0'
use_frameworks!
workspace 'AttachmentInput'

target 'AttachmentInput' do
  project 'AttachmentInput/AttachmentInput.xcodeproj'
  pod 'RxSwift', '6.0.0'
  pod 'RxCocoa', '6.0.0'
  pod 'RxDataSources', '5.0.0'
end

target 'Example' do
  project 'Example/Example.xcodeproj'
  pod 'RxSwift', '6.0.0'
  pod 'RxCocoa', '6.0.0'
  pod 'RxDataSources', '5.0.0'
end

post_install do |lib|
  lib.pods_project.targets.each do |target|
      target.build_configurations.each do |config|
          config.build_settings.delete 'IPHONEOS_DEPLOYMENT_TARGET'
      end
  end
end
