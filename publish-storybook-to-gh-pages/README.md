# Publish Storybook to GitHub Pages

A configuration that:

- Runs `eslint` and `stylelint`
- Runs `jest` tests with `--ci` so that [jest doesn't create new snapshots](https://jestjs.io/docs/en/cli.html#--ci)
- Runs `jest` with 1 worker per CPU (2/2) because these frontend tests are all CPU
- Allows each job to have its own cache by adding the workflow job id as a parameter in the cache key.
  Without this key, the storybook build will never get cached.
- Deploys storybook to your `gh-pages` branch using [storybook-deployer](https://github.com/storybookjs/storybook-deployer)
  - Only deploys storybook if your tests pass on master
- Separates the build and deploy commands so you know which one is slow or fails
