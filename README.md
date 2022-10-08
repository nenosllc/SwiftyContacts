# SwiftyContacts

[![Language: Swift 5](https://img.shields.io/badge/language-Swift%205-f48041.svg?style=flat-square)](https://developer.apple.com/swift)
[![License](https://img.shields.io/cocoapods/l/SwiftyContacts.svg?style=flat-square)](http://cocoapods.org/pods/SwiftyContacts)
[![Swift Package Manager](https://img.shields.io/badge/Swift%20Package%20Manager-compatible-brightgreen.svg?style=flat-square)](https://github.com/apple/swift-package-manager)

A Swift library for Contacts framework.

- [SwiftyContacts](#swiftycontacts)
  - [Requirements](#requirements)
  - [Installation](#installation)
    - [Swift Package Manager](#swift-package-manager)
  - [Get started](#get-started)
    - [async-await](#async-await)
      - [Requests access to the user's contacts](#requests-access-to-the-users-contacts)
      - [Request the current authorization status](#request-the-current-authorization-status)
      - [Fetch all contacts from device](#fetch-all-contacts-from-device)
  - [License](#license)

## Requirements

- iOS 15+ / Mac OS X 12+
- Xcode 14.0+

## Installation
The [Swift Package Manager](https://swift.org/package-manager/) is a tool for automating the distribution of Swift code and is integrated into the `swift` compiler. It is in early development, but SwiftyContacts does support its use on supported platforms.

Once you have your Swift package set up, adding SwiftyContacts as a dependency is as easy as adding it to the `dependencies` value of your `Package.swift`.

```swift
dependencies: [
    .package(url: "https://github.com/nenosllc/SwiftyContacts.git", .upToNextMajor(from: "2.0.0"))
]
```

## Getting Started
More documentation can be found by downloading the project and building the Xcode DocC documentation from Xcode.

### async-await

#### Requests access to the user's contacts
```swift
let access = try await requestAccess()
```

#### Request the current authorization status
```swift
let status = authorizationStatus()
print(status == CNAuthorizationStatus.authorized)
```

#### Fetch all contacts from device
```swift
let contacts = try await fetchContacts()
```

## License
SwiftyContacts is available under the MIT license. See the LICENSE file for more info.
