# Mobile app for administering Cortex Internet of Things.

This repository is intended for use by Cortex-App developers, to build and add your own features to the mobile app.

The app uses [Cordova][cordova] to develop in web technologies, producing iOS and Android builds from one codebase.

## Building

[Composer][composer] is used to manage code dependencies. Once Composer is installed, you can quickly get set up by running `composer install` from the project's root directory.

All of the build process that transform source web technologies into native mobile code are run by Composer using the `composer build` command. The source files of the app are contained within the `src/` directory, and the built mobile code is put into the `app/` directory.

Once build, an Android APK is available within `app/platforms/android` and an Apple IPA is available within `app/platforms/ios`.

Note that the Android and iOS SDKs must be present on the build system for builds to succeed. Builds will be skipped for platforms with missing SDKs.

## App code

All app content is provided by the [Neuron API][neuron].

## Running locally

[Composer][composer] is used to manage code dependencies. Once Composer is installed, you can quickly get set up by running `composer install` from the project's root directory.

Once installed, the app can be ran locally within a web browser by executing `vendor/bin/serve`. This will start a lightweight webserver on your computer that is accessible at http://localhost:8080

During local development, authentication is disabled and your public and private IP addresses are used to identify you to Neuron API calls.

[composer]: https://getcomposer.org
[neuron]: https://github.com/ArtificialMinds/Neuron