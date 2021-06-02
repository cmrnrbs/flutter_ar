# flutter_ar

A new Flutter project with AR Foundation.

This project using flutter_unity_widget and build with Flutter 2.2

## Getting Started

I fixed Demo AR Unity Project Editor/Build.cs file. Also android folder inside files : 

- settings.gradle
- build.gradle
- app/build.gradle

# Attention

- For build.gradle file, it's not saying flutter_unity_widget documentation but you can add unityLibrary/libs directory with flatDir. If you do not add this line, you will not be able to see the files.

- Dont forget to  move unity-classes folder inside the android folder.

- minSdkVersion must be at least 24. (For flutter app)

- I am not sure but in the documentation, said for Android <br/><br/>"Open the lib/architecture/ folder and check if there are both libUnityARCore.so and libarpresto_api.so files. There seems to be a bug where a Unity export does not include all lib files. If they are missing, use Unity to build a standalone .apk of your AR project, unzip the resulting apk, and copy over the missing .lib files to the unityLibrary module.". <br/><br/>I applied this step. and i must write pickFirst inside app/build.gradle. because if you can not add this lines, there will be error.

- For iOS Open the ios/Runner/Info.plist and change the following:
```
<dict>
+        <key>Privacy - Camera Usage Description</key>
+        <string>$(PRODUCT_NAME) uses Cameras</string>
</dict>
```
     

# Conclusion

I hope so you will be success.<br/>
Happy Coding :)