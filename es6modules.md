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
Webpack is used to compile JavaScript modules

## Explain what the concepts “entry” and “output” mean as relates to webpack
## Briefly explain what a development dependency is
## Explain what “transpiling code” means and how it relates to frontend development
## Briefly describe what a task runner is and how it’s used in frontend development
## Describe how to write an npm automation script
## Explain one of the main benefits of writing code in modules
## Explain “named exports” and “default exports”
