# CRA with API

A Create React App project that comes with its own Node Server and a bunch of useful scripts.

See live demos of branches:
- [master](https://cra-with-api-aehkwjfuwc.now.sh)
- [react-router](https://cra-with-api-zvunbytmru.now.sh)

## Key Features

- `./` (Project Root)

  - Yarn Workspaces used to hoist all workspace dependencies

    - NPM scripts for:
    - setting the name of the project (in `package.json` and `client/public/manifest.json`)
    - checking the current node version is latest Node version
    - setting the current Node version as the Node version for the project
    - checking if dependencies are up to date
    - updating dependencies to their latest versions in all `package.json` files
    - see disk usage of the client build
    - running client, server or both in development mode
    - generating a production build
    - running the production build
    - deploying production build using ∆Now

  - The following NPM packages that apply to both Client and Server workspaces:
    - [Prettier](https://prettier.io/) - apply consistent stying across client and server
    - [Gitmoji](https://gitmoji.carloscuesta.me/) - pretty git messages

- `./client`

  - Create React App
  - Dependencies manager by Yarn workspace

- `./server`

  - Run in development mode with Nodemon and Babel 7
  - Production build compiled with Babel 7
  - core-js is a dependency to enable the polyfills added by babel to be installed in production

- `./scripts`

  - Bash scripts for:
    - Killing the dev server process by port (for those times it doesn't terminate properly)
    - Prefixing `npx` to the gitmoji `prepare-commit-msg` hook, so gitmoji can be installed locally
    - Listing all the Now∆ deployments of the project
    - Removing all but the latest Now∆ deployment
    - Git Merging `master` into all other branches

## Debugging in WebStorm
- Client code
    - [Debugging React apps created with Create React App in WebStorm](https://blog.jetbrains.com/webstorm/2017/01/debugging-react-apps/)
    - TL;DR Create a new JavaScript Debug Run/Debug Configuration on the same URL the React App runs on

- Server code
    - [Debugging Node.js apps in WebStorm](https://blog.jetbrains.com/webstorm/2017/09/debugging-node-js-apps-in-webstorm/)
    - TL;DR Create a new Node.js Run/Debug Configuration

## Medium articles about this project

- [Create React App / Express API / Yarn Workspaces / Babel 7 / Now Deployment](https://medium.com/@smrgrace/create-react-app-express-api-yarn-workspaces-babel-7-now-deployment-2097bf8b371)
= [Having a git repo that is a template for new projects](https://medium.com/@smrgrace/having-a-git-repo-that-is-a-template-for-new-projects-148079b7f178)
