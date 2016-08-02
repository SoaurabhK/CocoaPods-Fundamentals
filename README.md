# CocoaPod-FundaMentals
This repository contains essentials for setting-up and using CocoaPods

    $ sudo gem update -n /usr/local/bin

    $ sudo gem install -n /usr/local/bin cocoapods

    $ pod setup      //this will download each podspec file from official cocoapod repositary to your machine.

    $ pod init  // initializes the Podfile

or start with empty file

    $ touch Podfile

    $ vi Podfile    // to edit it

What's Inside Podfile

    platform :osx, '10.7'
    use_frameworks!
    target “SkyFontsService” do
    pod 'PubNub', '3.7.11'
    end


Installing Same Pods for Multiple Targets

    platform :ios, '9.0'    
    use_frameworks!
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

Installing pod to a specific project-target in a workspace
And, For multiple targets we can use the same technique as mentioned above

```
workspace 'MyWorkSpace.xcworkspace'
use_frameworks!

target "TargetName" do
	platform :osx, '10.7'
	project "ProjectDir/Project.xcodeproj"
    pod 'PubNub', '3.7.11'
end
```    

// To search for libraries using terminal

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

http://stackoverflow.com/questions/22429383/how-do-i-configure-my-project-for-cocoa-pods-correctly

http://stackoverflow.com/questions/26394463/cocoapods-in-subproject

https://github.com/CocoaPods/CocoaPods/issues/738#issuecomment-15675099

https://github.com/CocoaPods/CocoaPods

https://github.com/CocoaPods/CocoaPods/issues/2413
