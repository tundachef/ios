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
