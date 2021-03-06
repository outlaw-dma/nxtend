# Changelog

# 4.1.1

# Bug Fixes

- generate `__mocks__/` directory under `src/`
- generate `components/` and `pages/` directory under `src/`

# 4.1.0

# Features

- initialize plugin with `@nxtend/capacitor` 2.0.2

# 4.0.0

# Features

- update Ionic to 5.4.1
- add `ionic.config.json` to application
- update starter template

# BREAKING CHANGES

- don't install and configure Cypress Testing Library
- removed `disableSanitizer` flag from `application` schematic

# 3.1.0

# Features

- update `@nxtend/capacitor` to 1.1.0
- update Ionic to 5.3.2
- update Ionicons to 5.1.2
- update `@testing-library/cypress` to 7.0.0
- update `@testing-library/jest-dom` to 5.11.4
- update `@testing-library/user-event` to 12.1.5

# BREAKING CHANGES

- `@testing-library/cypress`
  - `get` and `query` queries (which have been deprecated) have now been removed. Use `find` queries only.
  - **TS**: TypeScript type definitions have been brought into this module and no longer needs to be referenced from DefinitelyTyped

# 3.0.5

## Bug Fixes

- improve null checks when updating `tsconfig.json` in application schematic to support Nx 10

# 3.0.4

## Bug Fixes

- fix `Collection @nrwl/react not found` error if `@nrwl/react` is not added manually

# 3.0.3

## Bug Fixes

- add `@nrwl/react` version based on the users Nx version
- don't unnecessarily add `@nxtend/ionic-react` dependency in `init` schematic
- add `@nxtend/capacitor` 1.0.0 instead of `*`

# 3.0.2

## Bug Fixes

- properly initialize Capacitor plugin

# 3.0.1

## Features

- upgrade Ionic to 5.2.3

# 3.0.0

## Features

- generate Capacitor project with application by default
- upgrade `@testing-library/jest-dom` to 5.11.0
- upgrade `@testing-library/user-event` to 12.0.11

## Breaking Changes

- `@testing-library/user-event` was upgraded two major versions ([11.0.0](https://github.com/testing-library/user-event/releases/tag/v12.0.0)) ([12.0.0](https://github.com/testing-library/user-event/releases/tag/v12.0.0))

# 2.2.0

## Bug Fixes

- fix pascal case generate App unit test
- fix generating global styles for Emotion

## Features

- upgrade Ionic to 5.2.2
- add `--disableSanitizer` flag to application schematic to disable the [Ionic sanitizer](https://ionicframework.com/docs/techniques/security#sanitizing-user-input)

# 2.1.0

## Bug Fixes

- fix styled-components styles

## Features

- generate applications with ESLint instead of TSLint by default

# 2.0.0

## Features

- extend `@nrwl/react` schematics
- import `@testing-library/jest-dom` commands for unit tests
- upgrade `@testing-library/jest-dom` to 5.5.0
- upgrade `@testing-library/cypress` to 6.0.0
- upgrade `@testing-library/user-event` to 10.0.1
- honor `unitTestRunner` flag
- set `@nxtend/ionic-react` as the default collection if one is not set when generating an application
- honor `skipFormat` flag
- update Ionic starter template
  - [#1201](https://github.com/ionic-team/starters/pull/1201)
  - [#1202](https://github.com/ionic-team/starters/pull/1202)
  - [#1237](https://github.com/ionic-team/starters/pull/1237)

# 1.0.2

## Bug Fixes

- fix home page style import for pascal file name generated apps

## Features

- upgrade Ionic to 5.0.7
