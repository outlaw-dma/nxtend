---
id: getting-started
title: Getting Started
sidebar_label: Getting Started
---

Adding the `@nxtend/ionic-angular` plugin to your Nx workspace is trivial, and works just like any other Nx plugin.

## Initialize Plugin

```
# npm
npm install --save-dev --exact @nxtend/ionic-angular

# yarn
yarn add --save-dev --exact @nxtend/ionic-angular

# Nx CLI
nx generate @nxtend/ionic-angular:init

# Angular CLI
ng generate @nxtend/ionic-angular:init
```

## Generating Applications

Now, create your Ionic Angular application.

```
nx generate @nxtend/ionic-angular:application myApp
```

By default, a [Capacitor](../../docs/capacitor/overview.md) project will be generated that will allow you to compile your application as a native platform.

`@nxtend/ionic-angular` uses the `@nxtend/capacitor` plugin to add Capacitor support to an Ionic Angular application in an Nx workspace. By default, Capacitor configuration are added to new `@nxtend/ionic-angular` applications. To disable this, pass `--capacitor false` into the `@nxtend/ionic-angular` application schematic command.

Nx will ask you some questions about the application, but you can customize it further by passing these options:

```
nx generate @nxtend/ionic-angular:application [name] [options,...]

Options:
  --name                  The name of the application.
  --directory             The directory of the new application.
  --tags                  Add tags to the application (used for linting).
  --capacitor             Generate a Capacitor project. (default: true)
  --dryRun                Runs through and reports activity without writing to disk.
  --help                  Show available options for project target.
```

## Targets

Generated applications expose several functions to the CLI that allow users to build, lint, test, and so on.

```
nx build {frontend project name}
nx lint {frontend project name}
nx serve {frontend project name}
nx test {frontend project name}
nx e2e {frontend project name}-e2e
```

These applications are also supported by the Nx [affected](https://nx.dev/latest/angular/cli/affected#affected) commands.

## Add Native Platform

First, ensure that the frontend project has been built:

```
nx build {frontend project name}

nx build mobile-app
```

Now that a Capacitor project has been added to your Nx workspace you can begin adding support for native platforms. Currently, Capacitor supports Android and iOS, but other platforms can be added with Capacitor plugins.

```
nx run {frontend project}:add:ios
nx run {frontend project}:add:android
nx run {frontend project}:add --platform {native platform}

nx run my-app:add:android
```

## Open Native Platform

Finally, you can open the native platform in it's respective IDE:

```
nx run {frontend project}:open:ios
nx run {frontend project}:open:android
nx run {frontend project}:open --platform {native platform}

nx run my-app:open:android
```

To learn more about using Capacitor with `@nxtend/capacitor` then visit the [Getting Started](../capacitor/getting-started.md) page.

## Troubleshooting

If you receive a `Collection cannot be resolved` error when attempting to generate an application then you likely need to execute the [`@nxtend/ionic-angular:init`](./schematics/init) schematic.
