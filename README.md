# ffmpeg-android-maker

Here is a script that downloads the source code of [FFmpeg](https://www.ffmpeg.org) library and assembles it for Android. The script produces shared libraries as well as header files. The output structure looks like this:  
<img src="https://github.com/Javernaut/ffmpeg-android-maker/blob/master/images/output_structure.png" width="200">  
The actual content of all this directories depends on how the FFmpeg was configured before assembling. For my purpose I enabled only *libavcodec*, *libavformat*, *libavutil* and *libswscale*, but you can set your own configuration to make the FFmpeg you need.
The version of FFmpeg here is **4.1.4**. And the script expects to use at least Android NDK **r19** (*b* and *c* also work as well as *r20*). Starting with FFmpeg 4.1 and NDK r19 the whole process became much simpler.

## Supported architectures

* armeabi-v7a
* arm64-v8a
* x86
* x86_64

## Prerequisites

You have to define an environment variable `ANDROID_NDK_HOME` and set the correct path to your Android NDK.

## How to use

Well, just execute the script :) Examine the `output` directory after.

And the actual Android app can be found [here](https://github.com/Javernaut/WhatTheCodec)
