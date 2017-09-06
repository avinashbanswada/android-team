# Common Android Infrastructure

### Motivation

Standardizing things that provide no unique value to an application focuses our time on providing the unique value each application has, giving us a competitive edge in the market. Some choices are made not for convenience of the developers of the app themselves, but to reduce the pain or communication burden of others who care about our products.

Items listed here include tools, libraries, conventions, and processes.

## Table of Contents

* [Services](#services)
    * [Github — Code](#github-code)
    * [Fastlane — Automated build & deployment](#fastlane-automated-build--deployment)
    * [Jenkins — Continuous Integration](#jenkins-continuous-integration)
    * [OneSky — Translation](#onesky-translation)
    * [LaunchKit — AppReviews in Slack](#launchkit-appreviews-in-slack)
    * [CommHub — Internal push notification server](#commhub-internal-push-notification-server)
    
# Services

## Github — Code
The distributed version control and source code management (SCM) functionality of Git.
Source maintained at [Github Octanner](https://github.com/octanner)

## Fastlane — Automated build & deployment
> We use fastlane to automate pushing apk to beta and production in jenkins build scripts.

Fastlane is the tool to release Android app and handles all tedious tasks, like generating screenshots, dealing with code signing, and releasing application.

## Jenkins — Continuous Integration
Jenkins is a software that allows continuous integration. 
Android builds are performed automatically after every code commit done in github located at [iosbuild](http://iosbuild.octanner.com:8080/)

## OneSky — Translation

[OneSky](https://www.oneskyapp.com/): Translation Made Easy
for Apps, Games and Websites

_It's awesome because:_

Their workflow is very mobile-centric, and their translators are pretty good to work with. You can switch translators at anytime if you have an issue. There's no retainer fee, you simply pay per translation order. They offer glossary tools, as well as translation memory. You can create separate projects for iOS, App Store, and Android under a single product group.

Translations can be uploaded and downloaded as part of our Fastlane build process.

* Upload your strings early in the feature development, and send off an order. It's not uncommon for translations to take 3-4 business days for less common languages.
* Use standardized error messages. These are the single biggest place that iOS and Android strings drift apart, since the UI spec is the same for both apps.


## ReviewBot — AppReviews in Slack

[ReviewBot](https://reviewbot.io/): Monitor & Analyze Your Online Reviews
Get notified via Slack, Email, Trello, or Zendesk

_It's awesome because:_

It's so easy to keep tabs on what users think of your app! Just set it up and the reviews pour into your Slack channel for all to see.

_Tips & Conventions:_

_People it helps:_

* Product: they see how users are reacting to the app
* iOS devs: bug reports often happen in app reviews

_Alternatives we don't want to use:_

* Manually checking Play Store or the Play Store app
* [AppBot](https://appbot.co/), just because it costs more money. Reevaluate when review volumes across apps are high.


## CommHub — Internal push notification server

[Communication Hub](https://github.com/octanner/communication-hub): An internal server to send email, push notifications, and text messages to the customers of any of our apps.

_It's awesome because:_

It lets the server-side apps decide when and how to communicate to customers, and it's written once and then consistently used across all apps we create.

_Tips & Conventions:_

1. Use this in conjunction with the [Register Device](common-patterns.md#register-device) pattern.
1. `POST` the device info with the endpoint, auth, and payload listed in the docs.
1. Work with product and API groups to define the exact interactions they want in more sophisticated notifications.
1. Handle translation client-side for well-established notifications.

_People it helps:_

* Users: they get awesome interactions with the app.
* Product: they can work with the backend to create any kind of basic notification without android involvement.
* Enterprise IT: they can work out security and other concerns centrally.

