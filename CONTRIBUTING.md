# Contributing

## Setting up your development environment

The recommended way to setup your development environment for this repo is to open it in a
[GitHub Codespace](https://github.com/features/codespaces). 

### Codespace requirements

Literally all you need is either:
- a web browser, or
- VS Code (recommended)

[Web browser Codespaces documentation](https://docs.github.com/en/codespaces/developing-in-a-codespace/developing-in-a-codespace?tool=webui#working-in-a-codespace-in-the-browser)

[VS Code Codespaces documentation](https://docs.github.com/en/codespaces/developing-in-a-codespace/developing-in-a-codespace?tool=vscode#working-in-a-codespace-in-vs-code)

All you need to do is click on the green `<> Code` dropdown button on the GitHub repo page,
and then choose: `Create codespace on main`.

## Playwright tests

### Setting up Playwright

Playwright (and the browsers it needs) are installed automatically when the Codespace
first starts.  It takes a couple of minutes for the installation to complete, but it's a
one-time thing. (In the future we can avoid waiting by moving the installation process on to a
Docker container).

### Running the Playwright tests

#### Running the Playwright tests in VS Code

The Codespace comes with Playwright's VS Code extension already installed and configured.
To run the tests via the extension see the [Getting Started guide](https://playwright.dev/docs/getting-started-vscode)
and [the extension's documentation](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright).

#### Running the Playwright tests from the command line

- `npx playwright test`

### Running the Playwright tests in UI mode (from the GitHub Codespace)

Playwright's [UI mode is very powerful indeed](https://playwright.dev/docs/test-ui-mode), so it is important
that we can use this mode when working in a GitHub Codespace.  Fortunately, it is very easy to do so:

- `npx playwright test --ui-host=0.0.0.0`

As per [the documentation](https://playwright.dev/docs/test-ui-mode#docker--github-codespaces) the port gets
forwarded automatically, so it is then just a case of clicking on the link that is prompted in the terminal 
window - easy!

#### Limitations

- The tests only run in headless mode at the moment.  Should be able to have headed mode
  (and UI mode, debug mode, trace mode etc) working very soon, too.

## Linting and formatting

We use [Biome](https://biomejs.dev/) as a unified tool for both linting and formatting. It's a 
next-generation [opinionated](https://biomejs.dev/formatter/option-philosophy/) formatter and linter.
It is extremely fast and by using one tool for both formatting and linting we avoid the
[conflicts](https://dev.to/studio_m_song/how-to-make-eslint-work-with-prettier-avoiding-conflicts-and-problems-57pi)
that can often arise when using Prettier and ESLint.

The Codespace comes with [Biome's VS Code extension](https://biomejs.dev/reference/vscode/)
already installed and configured.  It is setup to
[format on save](https://biomejs.dev/reference/vscode/#format-on-save).

We also have a Biome CI check (a 
[Biome GitHub Action](https://biomejs.dev/recipes/continuous-integration/#github-actions)) that runs on all pushes and pull requests, to ensure that we are always fully compliant with Biome.
