# Node Server

For your backend node services.

- Sets up both PostgreSQL and Redis databases.
- Runs tests on the current LTS version used in production (currently 12) and the upcoming LTS version (currently 14).
- Sets the maximum number of workers to 4. Although GitHub Actions are allocated 2 CPUs, we suspect increasing the worker count would make the tests run faster because of the many external API calls these tests make. Adjust the number accordingly.
