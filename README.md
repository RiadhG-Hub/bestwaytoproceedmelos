
# BestWayToProceed

A comprehensive project designed to assist blind individuals by utilizing a phone camera and the Gemini AI system to determine whether it is safe to proceed. This project is divided into three sub-projects: `front`, `core`, and `analyze`.

## Sub-Projects

### BestWayToProceedFront

A Flutter Application designed to assist blind individuals by utilizing a phone camera and the Gemini AI system to determine whether it is safe to proceed. This package leverages advanced AI technology to provide real-time feedback and enhance the safety and independence of visually impaired users.

#### Features

- Capture images using the phone camera.
- Analyze images with the Gemini AI system.
- Provide audio feedback on whether it is safe to proceed.
- User-friendly interface designed for accessibility.
- Walk detector by measuring customizable phone shaking factors to auto-capture the image.
- Press volume up to take and analyze a picture.
- Press volume down to detect objects in the taken picture.
- Press volume down twice quickly to describe an alternative way.

#### Getting started

##### Prerequisites

- Flutter SDK: Ensure you have Flutter installed. You can download it [here](https://flutter.dev/docs/get-started/install).
- Dart SDK: Make sure Dart is installed and up to date.
- Device with a camera.
- Internet connection for AI processing.

##### Setting up the .env file

To run this application, you need to add a `.env` file with the following structure under `my-melos-repo/packages/bestWaytoproceedfront/`:

```plaintext
# Android API Key
ANDROID_API_KEY=AIzaSyCqX9bgBXnD8khc-SqF64KmwR0cNcwSn68

# iOS API Key
IOS_API_KEY=AIzaSyBe4x5toAJEWGZ7m3j70zs9FK3g2ODxiCU

# App ID
APP_ID=1:224943458926:ios:1cae748a9238287ef2747f

# Gemini API Key
GEMINI_API_KEY=AIzaSyA2sQyyq3cYUqakisqqzkrTENm7GWu8w7g

# Sentry DNS
SENTRY_DNS=https://4de90847a02b4296bf87ec02f1bf2513@o4505228691832832.ingest.us.sentry.io/4505228692750336
```

##### Contributing

We welcome contributions!

##### Filing Issues

If you encounter any issues, please file them [here](https://github.com/riadhrahma/bestWaytoproceedfront/issues). Our team will respond as quickly as possible.

For further inquiries or support, reach out to [gharbiriadh16@gmail.com](mailto:gharbiriadh16@gmail.com).

### BestWayToProceedCore

The core logic and algorithms powering the BestWayToProceed application, including the integration with the Gemini AI system and the processing of image data to determine safety and provide navigation advice.

#### Features

- Integration with the Gemini AI system.
- Processing of image data to determine safety.
- Calculation of safety percentages and navigation advice.
- Generation of detailed JSON responses.

#### Getting started

##### Prerequisites

- Dart SDK: Make sure Dart is installed and up to date.
- Internet connection for AI processing.

#### Additional information

For more information, please visit our [documentation](https://github.com/riadhrahma/bestWaytoproceedcore/doc).

##### Contributing

We welcome contributions!

##### Filing Issues

If you encounter any issues, please file them [here](https://github.com/riadhrahma/bestWaytoproceedcore/issues). Our team will respond as quickly as possible.

For further inquiries or support, reach out to [gharbiriadh16@gmail.com](mailto:gharbiriadh16@gmail.com).

### BestWayToProceedAnalyze

A backend service responsible for analyzing images captured by the BestWayToProceedFront application. This service leverages the Gemini AI system to provide detailed analysis and feedback.

#### Features

- Analysis of images using the Gemini AI system.
- Generation of detailed JSON responses including safety percentages, navigation advice, and object descriptions.
- Support for various image analysis scenarios including safety checks and object detection.

#### Getting started

##### Prerequisites

- Dart SDK: Make sure Dart is installed and up to date.
- Internet connection for AI processing.

#### Additional information

For more information, please visit our [documentation](https://github.com/riadhrahma/bestWaytoproceedanalyze/doc).

##### Contributing

We welcome contributions!

##### Filing Issues

If you encounter any issues, please file them [here](https://github.com/riadhrahma/bestWaytoproceedanalyze/issues). Our team will respond as quickly as possible.

For further inquiries or support, reach out to [gharbiriadh16@gmail.com](mailto:gharbiriadh16@gmail.com).

---

## Melos: Essential for Managing Packages and Running the Application

This project uses [Melos](https://melos.invertase.dev/) for efficient package management and running scripts. Melos simplifies managing multiple packages within the `bestwaytoproceed` project and ensures a streamlined setup process.

### Melos Configuration (`melos.yaml`)

```yaml
name: bestwaytoproceed
packages:
  - packages/**

scripts:
  setting-up-project: |
    git clone https://github.com/riadhrahma/bestwaytoproceedfront.git packages/bestwaytoproceedfront
    git clone https://github.com/riadhrahma/bestwaytoproceedcore.git packages/bestwaytoproceedcore
    git clone https://github.com/riadhrahma/bestwaytoproceedanalyze.git packages/bestwaytoproceedanalyze
    melos exec -c 1 -- "flutter pub get"
    cd packages/bestWaytoproceedfront
    echo "ANDROID_API_KEY=AIzaSyCqX9bgBXnD8khc-SqF64KmwR0cNcwSn68" > .env
    echo "IOS_API_KEY=AIzaSyBe4x5toAJEWGZ7m3j70zs9FK3g2ODxiCU" >> .env
    echo "APP_ID=1:224943458926:ios:1cae748a9238287ef2747f" >> .env
    echo "GEMINI_API_KEY=AIzaSyA2sQyyq3cYUqakisqqzkrTENm7GWu8w7g" >> .env
    echo "SENTRY_DNS=https://4de90847a02b4296bf87ec02f1bf2513@o4505228691832832.ingest.us.sentry.io/4505228692750336" >> .env
    flutter run --target lib/main.dart
  clone-packages: |
    git clone https://github.com/riadhrahma/bestwaytoproceedfront.git packages/bestwaytoproceedfront
    git clone https://github.com/riadhrahma/bestwaytoproceedcore.git packages/bestwaytoproceedcore
    git clone https://github.com/riadhrahma/bestwaytoproceedanalyze.git packages/bestwaytoproceedanalyze
  get: |
    melos exec -c 1 -- "flutter pub get"
  create-env: |
    cd packages/bestWaytoproceedfront
    echo "ANDROID_API_KEY=AIzaSyCqX9bgBXnD8khc-SqF64KmwR0cNcwSn68" > .env
    echo "IOS_API_KEY=AIzaSyBe4x5toAJEWGZ7m3j70zs9FK3g2ODxiCU" >> .env
    echo "APP_ID=1:224943458926:ios:1cae748a9238287ef2747f" >> .env
    echo "GEMINI_API_KEY=AIzaSyA2sQyyq3cYUqakisqqzkrTENm7GWu8w7g" >> .env
    echo "SENTRY_DNS=https://4de90847a02b4296bf87ec02f1bf2513@o4505228691832832.ingest.us.sentry.io/4505228692750336" >> .env
  run: |
    cd packages/bestwaytoproceedfront
    flutter run --target lib/main.dart -d ios
```

### Key Scripts

- **setting-up-project**: Clones all necessary packages, installs dependencies, sets up the `.env` file, and runs the Flutter application.
- **clone-packages**: Clones all the required repositories into the `packages` directory.
- **get**: Runs `flutter pub get` for all packages to fetch dependencies.
- **create-env**: Creates the `.env` file with necessary keys and values.
- **run**: Runs the Flutter application targeting the main entry point for iOS.

Melos automates the setup and execution process, making it easier for developers to get started and maintain the project. It ensures that all packages are properly configured and up-to-date, allowing you to focus on developing and enhancing the application's features.

Happy coding!
