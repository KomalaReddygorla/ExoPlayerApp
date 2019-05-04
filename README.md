# ExoPlayerApp

## ExoPlayer
ExoPlayer is an application level media player for Android.It provides an alternative to Android's MediaPlayer API for playing audio and video both locally and over the Internet.
ExoPlayer is an open source project that is not part of the Android framework and is distributed separately from the Android SDK. ExoPlayer’s standard audio and video components are built on Android’s MediaCodec API, which was released in Android 4.1 (API level 16).
Because ExoPlayer is a library, you can easily take advantage of new features as they become available by updating your app.

## Required
* Android Studio
* Java

## Dependencies
1. Add repositories
The easiest way to get started using ExoPlayer is to add it as a gradle dependency. You need to make sure you have the Google and JCenter repositories included in the build.gradle file in the root of your project:

```
repositories {
    google()
    jcenter()
}
```
2. Add ExoPlayer module dependencies
Next add a dependency in the build.gradle file of your app module. The following will add a dependency to the full library:

```
implementation 'com.google.android.exoplayer:exoplayer:2.X.X'
```
where ```2.X.X``` is your preferred version.
As an alternative to the full library, you can depend on only the library modules that you actually need. For example the following will add dependencies on the Core, DASH and UI library modules, as might be required for an app that plays DASH content:

```
implementation 'com.google.android.exoplayer:exoplayer-core:2.X.X'
implementation 'com.google.android.exoplayer:exoplayer-dash:2.X.X'
implementation 'com.google.android.exoplayer:exoplayer-ui:2.X.X'
```
The available library modules are listed below. Adding a dependency to the full library is equivalent to adding dependencies on all of the library modules individually.

* ```exoplayer-core```: Core functionality (required).
* ```exoplayer-dash```: Support for DASH content.
* ```exoplayer-hls```: Support for HLS content.
* ```exoplayer-smoothstreaming```: Support for SmoothStreaming content.
* ```exoplayer-ui```: UI components and resources for use with ExoPlayer.

In addition to library modules, ExoPlayer has multiple extension modules that depend on external libraries to provide additional functionality. Some extensions are available from JCenter, whereas others must be built manually.
