<h1>React Native Application End-to-End Testing with Maestro</h1>

This repository contains an example React Native application along with comprehensive end-to-end tests written using Maestro. Follow the steps below to set up the environment, write tests, and document the process.

<h2>Step 1: Generate the React Native Application:</h2>

Visit the Ignite GitHub repository here.
Follow the instructions to install the Ignite CLI.
Use the Ignite boilerplate to generate a new React Native application.

npx ignite-cli new MyReactNativeApp

<h2>Step 2: Set Up the Environment:</h2>

Ensure the React Native development environment is properly set up on your machine.
Install Maestro and any other necessary dependencies for testing.

npm install -g @maestro/testing

<h2>Step 3: Write Maestro Tests:</h2>

Familiarize yourself with Maestro’s syntax and features.
Identify key functionalities in the application that need testing.
Write end-to-end tests using Maestro, covering different scenarios and features of the application.

<b>Example Maestro test:</b>

import { test, expect } from '@maestro/testing';
import App from './App';

test('renders app correctly', async () => {
  const { getByText } = render(<App />);
  const textElement = getByText(/Hello, World!/i);
  expect(textElement).toBeTruthy();
});

<h2>Step 4: Documentation:</h2>

Document each step taken from setting up the environment to writing tests.
Ensure the documentation is clear and detailed enough for someone else to reproduce your steps.
Include screenshots or code snippets where necessary to enhance understanding.
See Documentation.md for detailed instructions and explanations.

# Maestro samples

`maestro download-samples` provides a set of flows and apps so that users can quickly set up a maestro test, without having to create an app.

download-samples downloads these files and apps from storage.googleapis.com.

# Update the samples

Although the samples are checked in, updating them requires a few manual steps:

* Change the samples in this directory and merge these changes
* Run `maestro download-samples`
* Copy *.yaml to the samples directory created by download-samples
* Run `(cd samples && zip -r "$OLDPWD/samples.zip" . -x "/**/.*" -x "__MACOSX")`
* Open https://console.cloud.google.com/storage/browser/mobile.dev/samples
* Upload samples.zip
* Adjust the permissions of samples.zip to "Public to Internet"
* Run `maestro download-samples` and verify that the change was successful
