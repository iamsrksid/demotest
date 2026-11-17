# selenium-tests

Automated UI tests recorded with **PulseQA Studio** and exported as a ready-to-run
**JavaScript · Mocha** project. Selenium Manager (built into Selenium 4) downloads
the matching ChromeDriver automatically, so no driver setup is needed.

## Requirements

Google Chrome and Node.js 18+.

## Run the tests

```bash
npm install
npm test
```

Run one test:

```bash
npx mocha tests/my-first.test.js
```

Run headless (no browser window), as CI does:

```bash
HEADLESS=true npm test
```

On Windows PowerShell use `$env:HEADLESS="true"` before the command.

Screenshots taken by the tests are written to `screenshots/`.

## Put it on GitHub

```bash
git init
git add .
git commit -m "Add Selenium tests"
git branch -M main
git remote add origin https://github.com/<your-user>/<your-repo>.git
git push -u origin main
```

The included workflow (`.github/workflows/selenium-tests.yml`) runs every test headless
on each push and pull request, and uploads screenshots as a build artifact.

## Test cases

### 1. My first test

   _(no steps)_

### 2. Test 2

   _(no steps)_

Readable test-case documents with screenshots are in [`docs/TEST_CASES.md`](docs/TEST_CASES.md).
BDD versions of each test are in `docs/features/`.
