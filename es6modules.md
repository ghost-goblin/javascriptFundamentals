# JavaScript - [ES6 Modules](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/es6-modules)

## Explain what npm is and where it was commonly used before being adopted on the frontend
The `node package manager` is a command line tool that gives you access to a gigantic repository of plugins, libraries and tools.

## Describe what npm init does and what package.json is
The `package.json` makes it easier for others to manage and install. Packages published to the registry must contain a `package.json` file.
A `package.json` file:
1. Lists the packages your project depends on
2. Specifies versions of a package that your project can use using semantic versioning rules
3. Makes your build reproducible, and therefore easier to share with other developers
4. A `package.json` file must contain `name` and `version` fields.

You can create a `package.jso`n file by running a CLI questionnaire or creating a default `package.json` file.
```sh
cd /path/to/package
```
and then run the following command
```sh
npm init
```

## Know how to install packages using npm
```sh
npm install <package_name>
```

## Describe what a JavaScript module bundler like webpack is
Webpack is used to compile JavaScript modules. When installing a package that will be bundled into your production bundle, you should use `npm install --save`.
If you're installing a package for development purposes (e.g. a linter, testing libraries, etc.) then you should use `npm install --save-dev`.

### `webpack` skeleton
```sh
├── dist
│   ├── main.js
│   └── index.html
├── src
│   └── index.js
├── package-lock.json
├── package.json
└── webpack.config.js
```

## Explain what the concepts “entry” and “output” mean as relates to webpack
An **entry point** indicates which module webpack should use to begin building out its internal dependency graph. `webpack` will figure out which other modules and libraries that entry point depends on _(directly and indirectly)_. By default its value is `./src/index.js`, but you can specify a different by setting an entry property in `webpack.config.js`.
```js
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```
The **output** property tells webpack where to emit the bundles it creates and how to name these files. It defaults to `./dist/main.js` for the main output file and to the `./dist` folder for any other generated file. You can configure this part of the process by specifying an output field in `webpack.config.js`.

## Briefly explain what a development dependency is
When you install an npm package using `npm install <package-name>`, you are installing it as a dependency and the package is automatically listed in the `package.json` file, under the `dependencies` list. When you add the `--save-dev`, you are installing it as a development dependency, which adds it to the `devDependencies` list.
Development dependencies are intended as development-only packages, that are unneeded in production. For example testing packages, webpack or Babel.
When you go in production, if you type `npm install` and the folder contains a `package.json` file, they are installed, as npm assumes this is a development deploy.
You need to set the `--production` flag to avoid installing those development dependencies.

## Explain what “transpiling code” means and how it relates to frontend development
Transpilers, or source-to-source compilers, are tools that read source code written in one programming language, and produce the equivalent code in another language.
Allow us to write compile-to-JavaScript languages, like CoffeeScript, TypeScript, or ClojureScript;

## Briefly describe what a task runner is and how it’s used in frontend development
## Describe how to write an npm automation script
You can add a `scripts` property to your `package.json` with the command you wish you run.
```js
"scripts": {
  "prostart": "./node_modules/protractor/bin/webdriver-manager start",
  "proupdate": "./node_modules/protractor/bin/webdriver-manager update"
}
```

## Explain one of the main benefits of writing code in modules
## Explain “named exports” and “default exports”
