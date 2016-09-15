platform :ios, '8.0'

target 'RxTodo' do
  use_frameworks!

  # Rx
  pod 'RxSwift', '~> 3.0.0-beta.1'
  pod 'RxCocoa', '~> 3.0.0-beta.1'
  pod 'RxDataSources', '~> 1.0.0-beta.2'

  # UI
  pod 'SnapKit', '3.0.0'
  pod 'ManualLayout', :git => 'https://github.com/devxoul/ManualLayout', :branch => 'swift-3.0'

  # Misc.
  pod 'Then', '2.0.0'
  pod 'ReusableKit', '1.0.0'
  pod 'CGFloatLiteral', '0.2.0'

  # Testing
  target 'RxTodoTests' do
    pod 'RxTests', '~> 3.0.0-beta.1'
    pod 'RxExpect', :git => 'https://github.com/devxoul/RxExpect', :branch => 'swift-3.0'
  end

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.0'
      config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.10'
    end
  end
end
