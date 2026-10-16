# SocietyHub

SocietyHub is a Java 21 web application with a React frontend.

## Continuous integration

The GitHub Actions workflow at `.github/workflows/societyhub-ci.yml` runs on
pushes and pull requests to `main`, and can also be started manually from the
repository's **Actions** tab.

The workflow verifies the Maven backend, installs frontend dependencies from
the lockfile, lints the React code, and builds both applications. Successful
runs publish the backend WAR and frontend `dist` directory as downloadable
artifacts for seven days. This is a build-and-validation pipeline; it does not
deploy to a hosting environment.

## Local requirements

- Java 21 and Maven
- Node.js 22 and npm

Run the backend verification with `mvn -B clean verify` from
`societyhub-backend`. In `societyhub-frontend`, run `npm ci`, `npm run lint`,
and `npm run build`.
