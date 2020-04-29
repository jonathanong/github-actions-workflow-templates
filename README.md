# Github Actions Workflow Templates

All of these templates include:

- Running tests on any commit push via `on: push:`
- Disabling npm logging except for errors with the `NPM_CONFIG_LOGLEVEL` and `NPM_CONFIG_PROGRESS` flags
- Maximize [node-gyp concurrency](https://github.com/nodejs/node-gyp/pull/1771) with the `NPM_CONFIG_JOBS` flag
- Caches eslint, stylelint, and jest artifacts to `node_modules/.cache` and saves it to the Action's cache
- Sets the appropriate number of jest workers based on the test type given the fact that GitHub Actions allocates 2 cpus
- Code coverage reporting support via [codecov.io](https://codecov.io/) and `npx codecov`
