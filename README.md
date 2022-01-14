# Getting Started

The project is a monorepo built with [yarn workspaces][workspaces] and [lerna][lerna]. All workspaces can be found under
the `packages` folder. Each package has its own readme file which contains detailed information about its content.

## Vertical micro-frontend
Are you interested in vertical split micro-frontends?

Take also a look at [micro-lc][micro-lc]!

### Set up the local environment

To develop the service locally you need:

- Node.js v14 or later,
- Yarn 1.x.x

To set up node.js, we suggest using [nvm][nvm], so you can manage multiple versions easily. Once you have installed nvm,
you can go inside the directory of the project and simply run `nvm install`, the `.nvmrc` file will install and select
the correct version if you don’t already have it.

To install Yarn, run `npm install --global yarn`.

Once you have all the dependency in place, you can launch:

```shell
yarn install
```

This command will install the dependencies for every workspace and will trigger a build of the [core](./packages/core/README.md)
workspace.

### Start the project

In order to try `micro-lc-element-composer` on your machine with mocked configurations, you have to execute only the `dev` script, using the following command:

```shell
yarn dev
```

### Run a package script

To run a script in a workspace, you can run `yarn workspace PACKAGE_NAME SCRIPT_NAME`. For example, to run tests in
[fe-container](./packages/fe-container/README.md) you should run:

```shell
yarn workspace fe-container test
```

or you can use the shortcut:

```shell
yarn fe-container test
```

[workspaces]: https://classic.yarnpkg.com/en/docs/workspaces/
[lerna]: https://github.com/lerna/lerna
[nvm]: https://github.com/creationix/nvm
[micro-lc]: https://github.com/micro-lc/micro-lc
