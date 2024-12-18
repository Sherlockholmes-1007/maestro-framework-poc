# Maestro Framework
Maestro is the simplest and most effective mobile UI testing framework.

# Why maestro
Maestro is built on learnings from its predecessors (Appium, Espresso, UIAutomator, XCTest) and allows you to easily define and test your Flows.

## Installation

Please refer to this link for installation

[maestro](https://maestro.mobile.dev/getting-started/installing-maestro)

---

## Table of Contents
1. [Introduction](#introduction)  
2. [Prerequisites](#prerequisites)  
3. [Installation](#installation)  
4. [Setup for Android](#android)  
5. [Setup for iOS](#ios)  
6. [Running Tests](#running-tests)  
7. [Troubleshooting](#troubleshooting)  
8. [Resources](#resources)  

---

## Introduction

Maestro is a lightweight mobile UI automation framework that uses simple YAML-based test scripts. This guide will help you set up Maestro on Android and iOS for efficient test execution.

---

## Prerequisites

Before proceeding, ensure the following tools are installed:

- **Java Development Kit (JDK) 11+**  
- **Node.js 14+**  
- **Homebrew** (for macOS users)  
- **Android Studio** (for Android testing)  
- **Xcode** (for iOS testing)  
- **Maestro CLI**  

## Installation

- Clone the project from the GitHub repository and checkout to the **master** branch
- Maestro Framework Installation - Refer to this [link](https://maestro.mobile.dev/getting-started/installing-maestro) to install Maestro frmaework depending upon the platform

> [!IMPORTANT]
> Make sure the maestro path is exported in Terminal / command as mentioned in the installation documentation


### Android Setup
- After installation of Android Studio, Open Android Studio > More Actions > Virtual Device Manager. Create your virtual device on the emulator based on the project dependency.

> [!NOTE]
> Always keep your android apps in the following directory -> resources/{android_app.apk}

### iOS Setup
- After installation of Xcode, Open Xcode > Click Xcode on the top right navigation bar > Open Developer Tool > Simulator > Open Simulator > pick any device (based on the project dependency)

> [!NOTE]
> Always keep your android apps in the following directory -> resources/{ios_app.app}


### Stream App Installation

### Android
**Command to Get App id**
```bash
  adb shell pm list packages
```
**Command to install Android app**
```bash
 adb install android_app.apk
```
_where adb denotes android debug bridge_

### iOS
Command to get all the simulators devices list
```bash
xcrun simctl list
```
Command to Boot iOS Simulator Device
```bash
   unzip sample.zip
   xcrun simctl install Booted Wikipedia.app
   maestro test ios-flow.yaml
```
Command to install iOS app
```bash
xcrun simctl install Booted {APP}
```
_where xcrun simctl denotes the simulator_

> [!NOTE]
> Virtual Devices need to be **BOOTED** before running tests so the virtual simulators will enable the boot device with id to run tests 

### Page Object Model
By Default Maestro frameworks supports Page Object pattern to support the reusable object mappings. Refer this [link](https://maestro.mobile.dev/examples/page-object-model) for more info.

### Finding Page Objects through Maestro Studio
Maestro framework uses **Maestro Studio** as a UI tool to find page object mappings in the Mobile apps. Refer this [link](https://maestro.mobile.dev/getting-started/maestro-studio) for more info.

### Install Platform-Specific Dependencies
- **For Android**: Install and configure `adb`.  
- **For iOS**: Ensure Xcode and provisioning profiles are properly set up.

---

## Running Tests

### Run Tests on Android
```bash
maestro test path/to/test.yaml
```

### Run Tests on iOS
```bash
maestro test path/to/test.yaml --device ios
```

### Use Interactive Mode
Launch Maestro Studio for exploring the app and recording actions:
```bash
maestro studio
```

---

## Troubleshooting

### Device Not Detected
- **For Android:** Ensure USB debugging is enabled and the device appears in `adb devices`.  
- **For iOS:** Ensure the device is trusted and visible in Xcode.

### App Installation Issues
- Verify the app file path and compatibility with the connected device.  
- For iOS, ensure the provisioning profile matches the device.

### Test Failures
- Check the YAML test script for errors.  
- Use `maestro studio` to debug and validate steps interactively.

---

## Resources

- [Maestro Documentation](https://maestro.mobile.dev/docs)  
- [Android Developer Guide](https://developer.android.com)  
- [iOS Developer Guide](https://developer.apple.com)  

---

With this guide, you should be able to set up and run Maestro for mobile automation. For further customization or issues, consult the official documentation or community forums.
```
