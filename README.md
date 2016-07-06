# CocoaPod-FundaMentals
This repository contains essentials for setting-up and using CocoaPods

$ sudo gem update -n /usr/local/bin
$ sudo gem install -n /usr/local/bin cocoapods
$ pod setup      //this will download each podspec file from official cocoapod repositary to your machine.

$ pod init  // initializes the Podfile

or start with empty file
$ touch Podfile
$ vi Podfile    // to edit it

Inside Podfile

platform :osx, '10.7'
target “SkyFontsService” do
    pod 'PubNub', '3.7.11'
end


Installing Same Pods for Multiple Targets
platform :ios, '9.0'
use_frameworks!
# My other pods
def testing_pods
    pod 'Quick', '0.5.0'
    pod 'Nimble', '2.0.0-rc.1'
end
target 'MyTests' do
    testing_pods
end 
target 'MyUITests' do
    testing_pods
end



// To search for libraries
$ pod search AFNetworking

or search in cocoapods.org in browser

// To Install dependencies 
$ pod install

After dependency installation use the xcworkspace instead of xcodeproj. 

References -
https://www.youtube.com/watch?v=iEAjvNRdZa0
https://www.youtube.com/watch?v=H-zK1mEwTe0
http://stackoverflow.com/questions/30812777/cannot-install-cocoa-pods-after-uninstalling-results-in-error/30851030#30851030
http://stackoverflow.com/questions/26351086/how-to-update-a-single-pod-without-touching-other-dependencies
http://stackoverflow.com/questions/34556991/pod-install-displaying-error-in-cocoapods-version-1-0-0-beta-1

Thanks!!!

