source 'https://github.com/CocoaPods/Specs.git'

platform :ios, '13.0'
use_frameworks!
inhibit_all_warnings!
workspace 'ghactions-poc.xcworkspace'

abstract_target 'GHActionsDependencies' do
  # https://github.com/getsentry/sentry-cocoa
  pod 'Sentry', '~> 5.1.10'

  target 'ghactions-poc'
  target 'ghactions-pocTests' do 
  	inherit! :search_paths
  end
end