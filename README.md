Disabling HDMI Check for Shaw Blue Curve TV
- enable streaming of Shaw BlueCurve TV app on android TV boxes

My workflow for disabling the HDMI check:

1. Downlaod APKTOOL from the link provided in the resource folder
   Decompile the app using apktool using the following command
   $ apktool d -r APPNAME.apk
   // decodes APPNAME.apk to APPNAME folder

2. Edit <̶d̶e̶c̶o̶m̶p̶i̶l̶e̶ ̶f̶o̶l̶d̶e̶r̶>̶/̶s̶m̶a̶l̶i̶_̶c̶l̶a̶s̶s̶e̶s̶2̶/̶c̶o̶m̶/̶x̶f̶i̶n̶i̶t̶y̶/̶c̶l̶o̶u̶d̶t̶v̶r̶/̶m̶o̶d̶e̶l̶/̶v̶i̶d̶e̶o̶/̶l̶o̶c̶k̶s̶/̶S̶e̶c̶o̶n̶d̶a̶r̶y̶D̶i̶s̶p̶l̶a̶y̶P̶l̶a̶y̶b̶a̶c̶k̶L̶o̶c̶k̶$̶2̶.̶s̶m̶a̶l̶i̶ <decompile folder>/smali_classes4/com/xfinity/cloudtvr/model/video/locks/SecondaryDisplayPlaybackLock$2.smali
   

3. Find the string "android.intent.action.HDMI_PLUGGED" and replace it with ""
   - In other words, delete android.intent.action.HDMI_PLUGGED leaving empty quotes
  
4. Recompile/build the app using apktool with the following command
   $ apktool b APPNAME -o NEW_APPNAME.apk
   // builds APPNAME folder into NEW_APPNAME.apk
   ***I've not been able to successfully recompile the apk and sign it proberly, so if anyone has a solution for that, I'd love to know what it is.

To sign the app properly I used the following steps:

5. Download APK Studio Editor and Use APK Studio Editor to unpack the modified recompile apk.( NEW_APPNAME.APK)

6. Copy the clsses4.dex and put it somewhere you remenber

7. Use APK Studio Editor to unpack the original apk.

8. Replace the classes4.dex file with the modded one.

9. Repack the apk with APK Studio Editor

10. Enjoy your working Blue Curve TV app on you android TV boxes
