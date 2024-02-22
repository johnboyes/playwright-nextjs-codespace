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
