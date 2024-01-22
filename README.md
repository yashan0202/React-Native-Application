React Native Application End-to-End Testing with Maestro

This repository contains an example React Native application along with comprehensive end-to-end tests written using Maestro. Follow the steps below to set up the environment, write tests, and document the process.

Step 1: Generate the React Native Application:

Visit the Ignite GitHub repository here.
Follow the instructions to install the Ignite CLI.
Use the Ignite boilerplate to generate a new React Native application.

npx ignite-cli new MyReactNativeApp

Step 2: Set Up the Environment:

Ensure the React Native development environment is properly set up on your machine.
Install Maestro and any other necessary dependencies for testing.

npm install -g @maestro/testing

Step 3: Write Maestro Tests:

Familiarize yourself with Maestro’s syntax and features.
Identify key functionalities in the application that need testing.
Write end-to-end tests using Maestro, covering different scenarios and features of the application.

Example Maestro test:

import { test, expect } from '@maestro/testing';
import App from './App';

test('renders app correctly', async () => {
  const { getByText } = render(<App />);
  const textElement = getByText(/Hello, World!/i);
  expect(textElement).toBeTruthy();
});

Step 4: Documentation:

Document each step taken from setting up the environment to writing tests.
Ensure the documentation is clear and detailed enough for someone else to reproduce your steps.
Include screenshots or code snippets where necessary to enhance understanding.
See Documentation.md for detailed instructions and explanations.
