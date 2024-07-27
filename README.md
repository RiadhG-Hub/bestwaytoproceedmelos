Here's the updated README file with the additional section for adding the `.env` file:

---

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

#### Additional information

For more information, please visit our [documentation](https://github.com/riadhrahma/bestWaytoproceedfront/doc).

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

Happy coding!