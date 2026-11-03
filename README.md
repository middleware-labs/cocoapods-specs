# Middleware CocoaPods Specs

CocoaPods specs for the Middleware iOS SDK (`MiddlewareRum`).

CocoaPods trunk stops accepting new pods on December 2, 2026, so new `MiddlewareRum` versions are published here. Versions already on trunk keep working.

## Install

Add both sources to the top of your `Podfile`. Keep the CocoaPods CDN source, because the SDK's dependencies still come from it.

```ruby
source 'https://github.com/middleware-labs/cocoapods-specs.git'
source 'https://cdn.cocoapods.org/'
```

Then install as usual:

```sh
pod install --repo-update
```

This covers native iOS, React Native and Flutter apps. In React Native and Flutter, add the lines to `ios/Podfile`.

## Publish a version

Run this after tagging the release in [middleware-ios](https://github.com/middleware-labs/middleware-ios):

```sh
pod repo add middleware-specs https://github.com/middleware-labs/cocoapods-specs.git
pod repo push middleware-specs MiddlewareRum.podspec --allow-warnings \
  --sources=https://github.com/middleware-labs/cocoapods-specs.git,https://cdn.cocoapods.org/
```
