# Whisper :leaves:

[![Version](https://img.shields.io/cocoapods/v/Whisper.svg?style=flat)](http://cocoadocs.org/docsets/Whisper)
[![License](https://img.shields.io/cocoapods/l/Whisper.svg?style=flat)](http://cocoadocs.org/docsets/Whisper)
[![Platform](https://img.shields.io/cocoapods/p/Whisper.svg?style=flat)](http://cocoadocs.org/docsets/Whisper)

## Description

Break the silence of your UI, whispering, shouting or whistling at it. **Whisper** is a component that will make the task of display messages and in-app notifications simple. It has three different views inside.

#### Whispers

![Whisper](https://github.com/hyperoslo/Whisper/blob/master/Resources/permanent-whisper.png)

Display a short message at the bottom of the navigation bar, this can be anything, from a "Great Job!" to an error message. It can have images or even a loader.

#### Shouts

![In-App](https://github.com/hyperoslo/Whisper/blob/master/Resources/in-app-notification.png)

Let the users know that something happened inside the app with this beautiful customizable in app notification.

#### Whistles

![Whistle](https://github.com/hyperoslo/Whisper/blob/master/Resources/whistle-information.png)

This is the smallest of all, a beautiful discretion in your UI.

##### Bonus

All the sounds are fully customizable, from colors to fonts.

Shouts have an optional action that will be called if the user taps on it, and you'll even get a message when the Shout is gone. Finally, if you want to set how long the Shout should be displayed, you have a duration property.

In Whisper, there is no need to think about scroll view insets anymore, this will be handled automatically. As and added bonus, when transitioning from one view controller to another, the next controllers offset will be adjusted like you would except. It just works!

## Usage

The usage of the component is so simple, you just create a message in the case of Whisper, an announcement in the case of a Shout or a Murmur in the case of a Whistle, it's done like this:

##### For a Whisper:

```swift
let message = Message(title: "Enter your message here.", color: UIColor.redColor())
Whisper(message, to: navigationController, action: .Present)
```

##### For a Shout:

```swift
let announcement = Announcement(title: "Your title", subtitle: "Your subtitle", image: UIImage(named: "avatar"))
Shout(announcement, to: self)
```

##### For a Whistle:

```swift
let murmur = Murmur(title: "This is a small whistle...")
Whistle(murmur)
```

## Installation

**Whisper** is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'Whisper'
```

## Roadmap

In the future the idea is to keep improving and add some features:

- Improve the offset detection and animation.
- Add more UI related components into Whisper.
- More customization points and more sizes for each whisper.
- Custom actions inside Whispers and Shouts.
- We are open to new and awesome ideas, contribute if you like! :)

## Author

Hyper Interaktiv AS, ios@hyper.no

## License

**Whisper** is available under the MIT license. See the LICENSE file for more information.
