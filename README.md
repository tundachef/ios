# ios
This is a repo highlighting the various debugs and ways to fix ios challenges, met when developing iphone apps.

## Problem: Cannot connect Iphone to Xcode || iphone connecting and disconnecting from mac

###### Top Solution: 
```
Head to Settings >
General > 
Reset on your iPhone and tap Reset Location & Privacy. (also Reset Network Settings)
```

Troubleshooting:
plug in your iPhone.
Open Xcode.
go to window -> Devices and Simulators.
Right click on your device.
click Unpair Device and unplug it.
restart Xcode.
restart your iPhone.
Connect your iPhone via USB.

## Problem: Flutter/Flutter.h' file not found 

```
flutter clean
pod deintegrate
flutter pub get
pod install
```

## Problem: Could not build module 'Gamekit' || Could not build module 'GameController' || 'GCPhysicalInputElement' is unavailable: not available on iOS

###### Top Solution: 
This looks like an Apple Issue in the Xcode 14.1 beta. I recommend sticking with Xcode 14.0 until Apple resolves it.

To workaround the issue with the Xcode 14.1 beta, if you're not using the GameCenter Firebase Auth provider, you can remove the file ```FirebaseAuth/Sources/AuthProvider/GameCenter/FIRGameCenterAuthProvider.m``` after installing Firebase and rebuild.

###### Ref: https://github.com/firebase/firebase-ios-sdk/issues/10231#issuecomment-1251146979

## Problem: Invalid Toolchain. Your app was built with an unsupported SDK or version of Xcode.

###### Top Solution: look at this picture
![Unsupported SDK or version of Xcode](/YEPpG.png)

## Problem: CocoaPods could not find compatible versions for pod "Flutter":
  In Podfile:
    Flutter (from `Flutter`)
![Couldn't find compatible versions for pod](/versionscreen.png)
###### Top Solution: Uncomment this line to define a global platform for your project
```
platform :ios, '11.0'
```

