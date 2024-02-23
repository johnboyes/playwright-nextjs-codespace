# Contributing

## Setting up Playwright

Playwright (and the browsers it needs) are installed automatically when the Codespace
first starts.  It takes a couple of minutes for the installation to complete, but it's a
one-time thing. (In the future we can avoid waiting by moving the installation process on to a
Docker container).

## Running the Playwright tests

### Running the Playwright tests in VS Code

The Codespace comes with Playwright's VS Code extension already installed and configured.
To run the tests via the extension see the [Getting Started guide](https://playwright.dev/docs/getting-started-vscode)
and [the extension's documentation](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright).

### Running the Playwright tests from the command line

- `npx playwright test`

## Limitations

- The tests only run in headless mode at the moment.  Should be able to have headed mode
  (and UI mode, debug mode, trace mode etc) working very soon, too.
