Disabling HDMI Check for Shaw Blue Curve TV
- enable streaming of Shaw BlueCurve TV app on android TV boxes

My workflow for disabling the HDMI check:

1. Decompile the app using apktool
2. Edit <decompile folder>/smali_classes2/com/xfinity/cloudtvr/model/video/locks/SecondaryDisplayPlaybackLock$2.smali
3. Find the string "android.intent.action.HDMI_PLUGGED" and replace it with ""
- In other words, delete android.intent.action.HDMI_PLUGGED leaving empty quotes
4. Recompile/build the app using apktool
***I've not been able to successfully recompile the apk and sign it proberly, so if anyone has a solution for that, I'd love to know what it is.
5. Use APK Studio Editor to unpack the recompile apk.
6. Copy the clsses2.dex and put it somewhere you remenber
7. Use APK Studio Editor to unpack the original apk.
8. Replace the classes2.dex file with the modded one.
9. Repack the apk with APK Studio Editor
10. Enjoy your working Blue Curve TV app on you android TV boxes
