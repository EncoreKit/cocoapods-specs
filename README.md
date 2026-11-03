# EncoreKit Specs

The CocoaPods spec repo for the Encore iOS SDK (`EncoreKit`) and its Objective-C overlay (`EncoreObjC`).

CocoaPods trunk becomes read-only on 2 December 2026, so new versions are published here only. This repo also holds every version that is on trunk, so one source resolves them all.

## Install

Add one line to your app target in the `Podfile`:

```ruby
pod 'EncoreKit', :source => 'https://github.com/EncoreKit/Specs.git'
```

Leave out the version when a wrapper (Unity, React Native, Flutter, Capacitor, KMP) pins it. With `:source`, CocoaPods looks for `EncoreKit` here only, and your other pods still resolve from trunk.

Do not add only `source 'https://github.com/EncoreKit/Specs.git'` at the top of the `Podfile`. A `source` line turns off the implicit trunk source, and CocoaPods takes a pod from the first source that has it. If you use `source` lines, list this repo first and trunk second:

```ruby
source 'https://github.com/EncoreKit/Specs.git'
source 'https://cdn.cocoapods.org/'
```

Unity: the Encore package adds the source for you through External Dependency Manager. You change nothing.

Swift Package Manager: use `https://github.com/EncoreKit/ios-sdk-binary` instead.

## Layout

`Specs/<Pod>/<version>/<Pod>.podspec.json`. The release script in the SDK repo adds each new version.
