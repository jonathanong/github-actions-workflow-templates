# Node Server

For your backend node services.

- Runs test on any commit push.
- Sets up both PostgreSQL and Redis databases.
- Runs tests on LTS and next upcoming LTS version.
- Disables npm logging except for errors.
- Maximize [node-gyp concurrency](https://github.com/nodejs/node-gyp/pull/1771) with the `NPM_CONFIG_JOBS` flag
- Saves eslint and jest caches to `node_modules/.bin/cache`.
- Sets the maximum number of workers to 4. Although GitHub Actions are allocated 2 CPUs, we suspect increasing the worker count would make the tests run faster because of the many external API calls these tests make.
