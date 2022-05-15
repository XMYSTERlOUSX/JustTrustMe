JustTrustMe
===========

<b>Changelog: 5/15/2022</b>

- Added support for Android 11! (By [gfbjngjibn](https://github.com/gfbjngjibn). You can check all the changes [here](https://github.com/Fuzion24/JustTrustMe/pull/59).)
- Support has been added for handling various errors on Android 7 and 11 (By [kasnder](https://github.com/kasnder). You can check all the changes [here](https://github.com/Fuzion24/JustTrustMe/pull/60/commits/9623835abb14bc5da801b08be7410a662afb4a9a).)
- A fix for OKHTTP 4.2.0+ has been added! (By [kasnder](https://github.com/kasnder). You can check all the changes [here](https://github.com/Fuzion24/JustTrustMe/pull/60/commits/b13d28e00c049227baeda139d29169588429bb2b).)
- Current version of the code has been updated to support compiling from android-sdk 30 + java 11 (By [tenwx1](https://github.com/tenwx1). You can check all the changes [here](https://github.com/Fuzion24/JustTrustMe/pull/60/commits/f010b76d8fcd6805c4b9412730a5c666aafe5bad).)

**You can find the pre-built release of this version** [here](https://github.com/XMYSTERlOUSX/JustTrustMe/releases/tag/V3).
===========

An xposed module that disables SSL certificate checking.  This is useful for auditing an application which does certificate pinning.  There also exists a nice framework built by @moxie to aid in pinning certs in your app: [certificate pinning](https://github.com/moxie0/AndroidPinning). 

An example of an application that does cert pinning is [Twitter](https://play.google.com/store/apps/details?id=com.twitter.android).  If you would like to view the network traffic for this application, you must disable the certificate pinning.

I built this for xposed rather than cydia substrate because xposed seems to support newer devices better. Marc Blanchou wrote the [original tool](https://github.com/iSECPartners/Android-SSL-TrustKiller) for cydia substrate.  If you find that you are not able to MITM an application please file an issue.

## Installation

As a prequsite, your device must be rooted and the xposed framework must be installed.
You can download the xposed framework [here](http://repo.xposed.info/module/de.robv.android.xposed.installer).

### Install from binary

The JustTrustMe binary can be downloaded from [https://github.com/Fuzion24/JustTrustMe/releases/latest](https://github.com/Fuzion24/JustTrustMe/releases/latest)

```
adb install ./JustTrustMe.apk
```

or navigate here and download the APK on your phone:
[https://github.com/Fuzion24/JustTrustMe/releases/latest](https://github.com/Fuzion24/JustTrustMe/releases/latest)


### Build from Source
All the normal gradle build commands apply:
To build a release APK:
```
./gradlew assembleRelease
```
To install directly to the phone connected via ADB:
```
./gradlew installRelease
```
