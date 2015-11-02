# OpenCV Face Detection Sample

opencvfacedetection-melvincabatuan created by Classroom for GitHub

This project illustrates OpenCV Face Detection sample in Android Studio.

## Prerequisite:

1. Download and extract OpenCV 3.0 for Android from http://opencv.org/.
2. Download and setup Android NDK build tools: http://developer.android.com/ndk/guides/setup.html
3. Create a new project in Android Studio with "No Activity" and add OpenCV to your project. (Refer to https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan)

## Possible Errors:

* OpenCV.mk not found Error 

* Solution:

Modify 'Android.mk' include as follows:

```make
include /path/to/your/OpenCV-android-sdk/sdk/native/jni/OpenCV.mk
```
Ex. 
```make
LOCAL_PATH := $(call my-dir)

include $(CLEAR_VARS)

#OPENCV_CAMERA_MODULES:=off
OPENCV_INSTALL_MODULES:=on
#OPENCV_LIB_TYPE:=SHARED

include /home/cobalt/Android/OpenCV-android-sdk/sdk/native/jni/OpenCV.mk

LOCAL_SRC_FILES  := DetectionBasedTracker_jni.cpp
LOCAL_C_INCLUDES += $(LOCAL_PATH)
LOCAL_LDLIBS     += -llog -ldl

LOCAL_MODULE     := detection_based_tracker

include $(BUILD_SHARED_LIBRARY)
```

## Compile 

Ex.
```shell
~/AndroidStudioProjects/OpenCV3-FaceDetection/app/jni$ ndk-build
[armeabi-v7a] Compile++ thumb: detection_based_tracker <= DetectionBasedTracker_jni.cpp
[armeabi-v7a] Prebuilt       : libopencv_java3.so <= /home/cobalt/Android/OpenCV-android-sdk/sdk/native/jni/../libs/armeabi-v7a/
[armeabi-v7a] SharedLibrary  : libdetection_based_tracker.so
/home/cobalt/Android/adt-bundle-linux-x86-20131030/android-ndk-r10d/toolchains/arm-linux-androideabi-4.8/prebuilt/linux-x86/bin/../lib/gcc/arm-linux-androideabi/4.8/../../../../arm-linux-androideabi/bin/ld: warning: hidden symbol '__aeabi_atexit' in /home/cobalt/Android/adt-bundle-linux-x86-20131030/android-ndk-r10d/sources/cxx-stl/gnu-libstdc++/4.8/libs/armeabi-v7a/thumb/libgnustl_static.a(atexit_arm.o) is referenced by DSO /home/cobalt/AndroidStudioProjects/OpenCV3-FaceDetection/app/obj/local/armeabi-v7a/libopencv_java3.so
[armeabi-v7a] Install        : libdetection_based_tracker.so => libs/armeabi-v7a/libdetection_based_tracker.so
[armeabi-v7a] Install        : libopencv_java3.so => libs/armeabi-v7a/libopencv_java3.so
```

## Accept

To accept the assignment, click the following URL:

https://classroom.github.com/assignment-invitations/f194ffd9123de302e38882178c375ccc

## Sample Solution:

https://github.com/DeLaSalleUniversity-Manila/opencvfacedetection-melvincabatuan

## Submission Procedure with Git: 

```shell
$ cd /path/to/your/android/app/
$ git init
$ git add –all
$ git commit -m "your message, e.x. Assignment 1 submission"
$ git remote add origin <Assignment link copied from assignment github, e.x. https://github.com/DeLaSalleUniversity-Manila/secondactivityassignment-melvincabatuan.git>
$ git push -u origin master
<then Enter Username and Password>
```


## Screenshot:

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvfacedetection-melvincabatuan/blob/master/device-2015-11-02-130507.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvfacedetection-melvincabatuan/blob/master/device-2015-11-02-130917.png)

"*If human beings had genuine courage, they'd wear their costumes every day of the year, not just on Halloween.*" - Douglas Coupland
