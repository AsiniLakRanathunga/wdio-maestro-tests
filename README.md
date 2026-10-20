# WDIO Native Demo App — Maestro Tests

## Overview
Android mobile UI automation for the WebdriverIO Native Demo App v2.2.0, created for a Senior QA Engineer (Mobile) take-home exercise.

## Why Maestro?
Maestro uses readable YAML flows for mobile interactions and assertions. It is quick to set up and suitable for native mobile smoke and functional testing.

## Prerequisites
- Java 17
- Maestro CLI
- Android SDK Platform-Tools (ADB)
- Android device with USB debugging enabled
- WebdriverIO Native Demo App v2.2.0 installed

Demo app release:
https://github.com/webdriverio/native-demo-app/releases/tag/v2.2.0

## Setup
1. Install Java, Android SDK Platform-Tools, and Maestro.
2. Install the demo app APK on an Android device.
3. Connect the device and approve the USB debugging prompt.
4. Verify the device with db devices.
5. Verify Maestro with maestro --version.

## Running tests
Run commands from the repository root:

- maestro test .\flows\smoke.yaml
- maestro test .\flows\signup.yaml
- maestro test .\flows\signup-invalid-email.yaml
- maestro test .\flows\signup-password-mismatch.yaml
- maestro test .\flows\login.yaml
- maestro test .\flows\login-invalid-email.yaml
- maestro test .\flows\login-short-password.yaml
- maestro test .\flows\forms.yaml
- maestro test .\flows\forms-switch.yaml
- maestro test .\flows\forms-active.yaml

## Test coverage

### Sign-up
- Successful registration and success dialog
- Invalid email validation
- Mismatched password validation

### Login
- Successful login and success dialog
- Invalid email validation
- Password shorter than eight characters

### Forms
- Text input is echoed
- Switch toggling updates its label
- Active button opens a native alert

## Project structure
lows/ contains the Maestro YAML test flows.

## Future improvements
- Verify all flows together and improve test reporting.
- Improve test-data management.
- Add more negative and boundary cases.
- Integrate with continuous integration.
- Add further device and OS coverage.

## AI usage disclosure
AI assistance was used for setup guidance, drafting and troubleshooting Maestro YAML flows, and documentation. The flows were executed against the demo app on a physical Android device, and assertions were adjusted based on observed behaviour. The author is responsible for reviewing, maintaining, and explaining the submitted work.
