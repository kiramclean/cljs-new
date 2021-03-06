# Cljs New

Generate the bare minimum you need for a new Clojurescript app that uses
shadow-cljs. This is _not_ intended to be an opinionated framework for new cljs
projects. The goal is simply to have a single command you can run to generate
the scaffolding without needing to create a bunch of files manually to get
started with cljs.

## Quickstart

    npx cljs-new my-app-name
    cd my-app-name
    yarn dev

Navigate to http://localhost:3000 to see your app. The boilerplate html you see
is in `public/index.html`.

To deploy to production, create a minified bundle with `yarn build`.

## Features

- No opinionated defaults. This creates a new project with no dependencies and makes no assumptions about how you will structure your app. It only sets up the bare minimum build chain required to start a new clojurescript project.
- [Chrome cljs devtools](https://github.com/binaryage/cljs-devtools) are included and configured, which allows you to work with clojurescript directly in the Chrome devtools.
  - **shadow-cljs uses [namespace dependency graphs](https://shadow-cljs.github.io/docs/UsersGuide.html#_dependencies) to determine what code is needed in the final output, so there is no need to specify dev dependencies separately**
- `dev`, `compile`, `release`, `browser-repl`, `node-repl`, and `test` commands already configured and ready to run with one command
<!-- - console logging disabled for production builds -- maybe? maybe should not worry about this -->

## Usage

Creating a new app (with `npx cljs-new my-app-name`) will create the following
files in a directory called `my-app-name`:

my-app-name
├── .gitignore
├── README.md
├── package.json
├── shadow-cljs.edn
├── public
|  ├── css
|  |  └── style.css
|  ├── index.html
|  └── favicon.ico
└── src
   └── app
      └── main.cljs

## Dependencies

You need node (a JavaScript runtime) and npm v5.2+ (a JavaScript package
manager, and more) installed on your machine. npm comes with node. [Here are
the node installation instructions](https://nodejs.org/en/download/package-manager/#macos).
