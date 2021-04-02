## Reading

Review the syllabus and post any questions on the Q&A forum

zyBooks Ch 1.1 - 1.4

Mobile devices include phones, tablets and smartwear (watches, rings).
The two most popular operating systems for mobile devices are Android (Google) and iOS (Apple).
The differences between the two operating systems have to do with open source vs. proprietary approach, as well different user interfaces. 
Android is available on various devices, manufactured by different manufacturers, therefore, the Android users experience differences in the UI between different
phones manufacturers, whereas Apple controls the iOS resulting in a similar style.
  
Worldwide, Android is the most popular mobile OS, whereas in the US the iOS is more popular than Android.

https://gs.statcounter.com/os-market-share/mobile/worldwide/#monthly-201706-201805

Mobile apps can be written for Android, iOS, or both.  Android apps can be downloaded from the Google Play Store.

Apps can be free or paid, or sometimes free with in-app purchases. Free apps monetize by displaying ads.

Enlisting an app on Google's play store costs $25 (one time). The app must pass a variety of pre-release requirements specified by Google before it can be published.
It is also possible to distribute apps from websites or directly (by sharing the APK file), however Android disables non Google Play app installations by default,
so most users do not install them.

When an app is created to run directly on an OS, it is referred to as native. 
Another approach is to create a web app that can run on a mobile devices.
Finally, a hybrid app might combine a web container and a native app.

The official Android development environment is Android Studio IDE (free to install). Apps can be written in Java, and more recently, in Kotlin, with the use of libraries 
from the Android SDK. 

Source code is compiled into bytecode by the Java (or Kotlin) compiler. The R8 compiler converts the bytecodes into optimized Dex bytecodes, which are then converted to
.oat files on the device with an ahead-of-time compiler. The Android Runtime(ART), a virtual machine, runs the .oat files.

In this class we will focus on writing apps in Java, a language you are already familiar with. 

Android has released multiple versions, with newer versions supporting various enhancements.
See a list of Android versions here: https://en.wikipedia.org/wiki/Android_version_history

An Android app consists of the of the following components:

* Activity: a single screen providing UI and user interaction.
* Service: non UI operation that runs in the background.
* Broadcast receiver: used to broadcast system wide announcements to the app
* Content provider: manages the app data

Android studio IDE components include a Layout editor, Theme editor,  Java/Kotlin editor, SDK Manager, Android Virtual Device(AVD) manager, Android emulator, and a Debugger.

Within the Android studio, there are projects, containing files, such as source code (Java or Kotlin) or XML. In addition, there is the Grade build tool,
which compiles files into an APK file.
An APK file is a compressed file containing the app. When you install an app on a device, it is the APK that is installed.

There are multiple types of files that are part of an Android project. They include:

* AndroidManifest.xml to specify information about the such as name, or permissions.

* Java files such as MainActivity.java, the main activity that runs when an app is started.

* The res folder contains the app's resources, such as layouts or text strings (considered resources by Android).

* The drawable folder is used for any images that are part of the app.

* The layout folder contains the XML layout files, which define the app's UI. For example, activity_main.xml is the corresponding layout file for MainActivity.

* The mipmap folder holds the app's launcher icons, which are displayed on the devices' home screen.

* The values folder contains key value pairs for colors, styles or strings.

* Gradle Scripts contains the build files for the app.

* The Android emulator, or Android Virtual Device (AVD) allows developers to run a simulation of an App without using an actual phone device.

## Reference

https://en.wikipedia.org/wiki/Android_(operating_system)

https://developer.android.com/studio/intro

## Practice

zyBooks Ch 1.1 - 1.4 Practice (graded participation activity)

## Learning Outcomes
Upon successful completion of the material, students wll be able to:

* Describe the Android mobile environment fundamentals

* Install and work with Android studio, APKs and emulators

* Create and run an Android app in Android studio (code provided)

