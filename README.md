# Place Tracker (beta)

A sample place tracking app that uses the
[google_maps_flutter](https://github.com/flutter/plugins/tree/master/packages/google_maps_flutter)
plugin. Keep track of your favorite places, places you've visited, and places
you want to go. View details about these places, show them on a map, and get
directions to them.

## IMPORTANT

### `place_map.dart`

This page shows a full-screen GoogleMap widget with place markers. Provides
examples of how to stack other widgets on top of a GoogleMap widget, how to add
markers to a map, and how to make other flutter widgets interact with the
GoogleMap widget.

### `place_details.dart`

This page shows a detailed view of a single place. Provides examples of how to
place a GoogleMap widget inside of a ListView and how to disable certain touch
gestures on the map.

## Getting Started

To run this sample app, you will need an API key.

Get an API key at <https://cloud.google.com/maps-platform/>.

### Android
Specify your API key in the application manifest
`android/app/src/main/AndroidManifest.xml`:

```xml
<manifest ...
  <application ...
    <meta-data android:name="com.google.android.geo.API_KEY"
               android:value="YOUR KEY HERE"/>
```

### iOS
Specify your API key in `AppDelegate.swift`:

```swift
@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
    GMSServices.provideAPIKey("YOUR API KEY HERE")
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
}
```

For additional help setting up the plugin, see the plugin's
[README](https://pub.dev/packages/google_maps_flutter)
page.

For help getting started with Flutter, view online
[documentation](https://flutter.io/).

## Note

The google_maps_flutter plugin is in developer preview until [dynamic thread
merging](https://github.com/flutter/flutter/projects/155) is finished.
