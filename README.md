# glaucoma_ui_api
This branch is for all the UI updates.

We need to add the following details in EyeCue-Info.plist under the platforms/ios/EyeCue

<key>LSApplicationQueriesSchemes</key>
<array>
    <string>eyecuegame</string>
    <string>game</string>
    <string>eyecandy</string>
    <string>fb</string>
</array>

<key>NSPhotoLibraryUsageDescription</key>
<string>This app requires access to the photo library.</string>
<key>NSMicrophoneUsageDescription</key>
<string>This app requires access to the microphone.</string>
<key>NSCameraUsageDescription</key>
<string>This app requires access to the camera.</string>

**************************************************
LOCAL NOTIFIATION ISSUE FIXES IN IOS 10
**************************************************

cordova plugin rm de.appplant.cordova.plugin.local-notification
cordova plugin add https://github.com/katzer/cordova-plugin-local-notifications#ios10

**************************************************
REMOTE PUSH NOTIFIATION UPGRADE CHANGES
**************************************************

ionic plugin rm phonegap-plugin-push
ionic plugin add phonegap-plugin-push@1.8.4 --variable SENDER_ID="xxxxxx"
ionic config set gcm_key "xxxxxx"
ionic config set dev_push false

**************************************************
ANDROID GAME DOWNLOAD ISSUE
**************************************************
We have to change the following line in platforms/android/AndroidManifest.xml

<uses-sdk android:minSdkVersion="16" android:targetSdkVersion="23" /> to 

<uses-sdk android:minSdkVersion="16" android:targetSdkVersion="21" />

**************************************************
MISSING PUSH NOTIFICATION ENTITLEMENT - iOS 
**************************************************
Make sure the bundle id should be "com.sheep.glaucoma" 

**************************************************
       STEPS TO CHECK AUTO UPDATE - Android
**************************************************
Current version is 1.5.2 (DB also it contains the last updated version as 1.5.2)
1. Take the build and rename it to eyecue.apk 
2. Upload the eyecue.apk file under the admin_portal/html/ directory & deploy it into the aws
3. Change the version number in config.xml which is lesser than the version 1.5.2 (downgrade the version)
4. Then take the build again and then check the auto update functionality in android