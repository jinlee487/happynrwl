# Happynrwl

This project was generated using [Nx](https://nx.dev).

This is a demo project to learn how to use nx to build typescript library, web and node apps.

We will be testing out building typescript library, web and node app.

        npx create-nx-workspace happynrwl --preset=ts

        happynrwl/
        ├── packages/
        ├── tools/
        ├── workspace.json
        ├── nx.json
        ├── package.json
        └── tsconfig.base.json

        npx nx generate @nrwl/js:library --name=hello-tsc --buildable

        npx nx lint hello-tsc

        > nx run hello-tsc:lint

        Linting "hello-tsc"...
        =============

        WARNING: You are currently running a version of TypeScript which is not officially supported by @typescript-eslint/typescript-estree.

        You may find that it works just fine,
        or you may not.

        SUPPORTED TYPESCRIPT VERSIONS: >=3.3.1 <4.7.0

        YOUR TYPESCRIPT VERSION: 4.7.4

        Please only submit bug reports when using the officially supported version.

        =============

        All files pass linting.

        ————————————————————————————————————

        > NX Successfully ran target lint
        > for project hello-tsc (4s)

            See Nx Cloud run details at https://nx.app/runs/5AWqF9VcZwc

        npx nx test hello-tsc

        > nx run hello-tsc:test

        PASS hello-tsc packages/hello-tsc/src/lib/hello-tsc.spec.ts
        helloTsc
        √ should work (2 ms)

        Test Suites: 1 passed, 1 total
        Tests: 1 passed, 1 total
        Snapshots: 0 total
        Time: 3.044 s
        Ran all test suites.

        ————————————————————————————————————

        > NX Successfully ran target test
        > for project hello-tsc (7s)

            See Nx Cloud run details at https://nx.app/runs/YE5E0EmJyHT

        npx nx build hello-tsc

        > nx run hello-tsc:build

        Compiling TypeScript files for project "hello-tsc"...
        Done compiling TypeScript files for project "hello-tsc".

        ————————————————————————————————————

        > NX Successfully ran target build for project hello-tsc (2s)

            See Nx Cloud run details at https://nx.app/runs/072oXhX1KpF

        The output of the build step is placed into the dist/packages/hello-tsc by default.

        npx nx report
        if @nrwl/node is not installed, then run
        npm i @nrwl/node --save

        run the application
        npx nx serve demoapp

        if @nrwl/web is not installed, then run
        npm i @nrwl/web --save

        npx nx serve demowebapp

        > nx run demowebapp:serve

        <i> [webpack-dev-server] Project is running at:
        <i> [webpack-dev-server] Loopback: http://localhost:4200/, http://127.0.0.1:4200/
        <i> [webpack-dev-server] 404s will fallback to '/index.html'

        > NX Web Development Server is listening at http://localhost:4200/

        // importing from hello-tsc
        import { helloTsc } from '@happynrwl/hello-tsc';

        // use the function

        console.log(helloTsc());

        console.log('Hello World!');

        npx nx serve demoapp
        Debugger listening on ws://localhost:9229/19ed6d94-3233-4e29-9a02-a405b6c753dc
        Debugger listening on ws://localhost:9229/19ed6d94-3233-4e29-9a02-a405b6c753dc
        For help, see: https://nodejs.org/en/docs/inspector
        hello-tsc
        Hello World!

<p style="text-align: center;"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-logo.png" width="450"></p>

🔎 **Smart, Fast and Extensible Build System**

## Adding capabilities to your workspace

Nx supports many plugins which add capabilities for developing different types of applications and different tools.

These capabilities include generating applications, libraries, etc as well as the devtools to test, and build projects as well.

Below are our core plugins:

- [React](https://reactjs.org)
  - `npm install --save-dev @nrwl/react`
- Web (no framework frontends)
  - `npm install --save-dev @nrwl/web`
- [Angular](https://angular.io)
  - `npm install --save-dev @nrwl/angular`
- [Nest](https://nestjs.com)
  - `npm install --save-dev @nrwl/nest`
- [Express](https://expressjs.com)
  - `npm install --save-dev @nrwl/express`
- [Node](https://nodejs.org)
  - `npm install --save-dev @nrwl/node`

There are also many [community plugins](https://nx.dev/community) you could add.

## Generate an application

Run `nx g @nrwl/react:app my-app` to generate an application.

> You can use any of the plugins above to generate applications as well.

When using Nx, you can create multiple applications and libraries in the same workspace.

## Generate a library

Run `nx g @nrwl/react:lib my-lib` to generate a library.

> You can also use any of the plugins above to generate libraries as well.

Libraries are shareable across libraries and applications. They can be imported from `@happynrwl/mylib`.

## Development server

Run `nx serve my-app` for a dev server. Navigate to http://localhost:4200/. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `nx g @nrwl/react:component my-component --project=my-app` to generate a new component.

## Build

Run `nx build my-app` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `nx test my-app` to execute the unit tests via [Jest](https://jestjs.io).

Run `nx affected:test` to execute the unit tests affected by a change.

## Running end-to-end tests

Run `nx e2e my-app` to execute the end-to-end tests via [Cypress](https://www.cypress.io).

Run `nx affected:e2e` to execute the end-to-end tests affected by a change.

## Understand your workspace

Run `nx graph` to see a diagram of the dependencies of your projects.

## Further help

Visit the [Nx Documentation](https://nx.dev) to learn more.

## ☁ Nx Cloud

### Distributed Computation Caching & Distributed Task Execution

<p style="text-align: center;"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-cloud-card.png"></p>

Nx Cloud pairs with Nx in order to enable you to build and test code more rapidly, by up to 10 times. Even teams that are new to Nx can connect to Nx Cloud and start saving time instantly.

Teams using Nx gain the advantage of building full-stack applications with their preferred framework alongside Nx’s advanced code generation and project dependency graph, plus a unified experience for both frontend and backend developers.

Visit [Nx Cloud](https://nx.app/) to learn more.
