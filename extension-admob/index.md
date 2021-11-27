---
layout: manual
language: en
github: https://github.com/defold/extension-admob
title: Defold AdMob extension API documentation
brief: This manual covers how to get use AdMob to show ads on iOS and Android in Defold.
---

# Defold AdMob extension API documentation

This extension provides a unified, simple to use interface to show AdMob ADS on iOS and Android.


## Installation
To use this library in your Defold project, add the following URL to your `game.project` dependencies and then fetch libraries using `Project->Fetch Libraries` :

[https://github.com/defold/extension-admob/archive/master.zip](https://github.com/defold/extension-admob/archive/master.zip)

We recommend using a link to a zip file of a [specific release](https://github.com/defold/extension-admob/releases).


## Setup

Before you begin you need to either [sign in](https://admob.google.com/home/) to or [sign up for](https://support.google.com/admob/answer/7356219) an AdMob account. Next you need to [register your app with AdMob](https://support.google.com/admob/answer/2773509) to get an AdMob App Id. You need this id when you configure your Defold game.


## Configuration
The extension can be configured by adding the following fields to `game.project` ( just open this file in any text editor and paste these lines):

```
[admob]
app_id_ios = ca-app-pub-3940256099942544~1458002511
app_id_android = ca-app-pub-3940256099942544~3347511713
ios_tracking_usage_description = Your data will be used to provide you a better and personalized ad experience.
```

### app_id_ios
This is your iOS AdMob app ID. An app ID is a unique ID number assigned to your apps when they're added to AdMob. The app ID is used to identify your apps.

### app_id_android
This is your Android AdMob app ID. An app ID is a unique ID number assigned to your apps when they're added to AdMob. The app ID is used to identify your apps.

### ios_tracking_usage_description

Before requesting the unique IDFA string for a device on iOS 14 the application must request user authorization to access app-related data for tracking the user or the device. This is done automatically when `admob.request_idfa()` is called. The string set in `admob.ios_tracking_usage_description` will be shown to the user.

Apple documentation: https://developer.apple.com/documentation/apptrackingtransparency?language=objc


## Example

[Refer to the example project](https://github.com/defold/extension-admob/blob/master/main/ads.gui_script) to check how itergation works.
Make sure you test example and you integration usingtest ADS units (see [init()](https://github.com/defold/extension-admob/blob/28452b6b49c6304b274a80070279768f89cab8ac/main/ads.gui_script#L157-L183) in the example)

Please, make sure you test AdMob on iOS or Android (on the other platforms `admob` table will be nil).

## Source code

The source code is available on [GitHub](https://github.com/defold/extension-admob)


## API reference
[API Reference](/extension-admob/api)