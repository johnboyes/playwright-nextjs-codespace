# Contributing

## Setting up Playwright

Playwright (and the browsers it needs) are installed automatically when the devcontainer
first starts.  It takes a couple of minutes for the installation to complete, but it's a
one-time thing.

## Running the Playwright tests

- `npx playwright test`

## Limitations

- The tests only run in headless mode at the moment.  Should be able to have headed mode
  (and UI mode, debug mode, trace mode etc) working very soon, too.

- The available browsers that the tests run on are:

  - Desktop Chrome
  - Mobile Chrome
  - Mobile Safari

    (not sure why the other browsers such as Firefox and WebKit are not available, haven't looked into this yet)
