# Open Source Module

For open source JS modules.
To be used in the browser, you may also want to run tests with `testEnvironment: jsdom` in `jest.config.js`.

- Runs tests on both commit pushes as well as pull request activity.
- Runs tests on LTS versions of node as well as the currently active versions of node.
- Saves eslint and jest caches to `node_modules/.bin/cache`.
- Sets the maximum number of workers to 2 as GitHub Actions are allocated 2 CPUs. You can increase this if your tests are less CPU-intensive and more concurrent (e.g. with external API calls or it has a lot of sleeps for some reason).
