# Test Driven Development

## [Jest](https://jestjs.io/docs/getting-started)
1. `npm init -y`
2. `npm install --save-dev jest`
3. Add to `package.json` to call Jest
```js
"scripts": {
  "test": "jest"
}
```
+ `npm add --dev babel-jest`

> Jest will treat any file that ends in `.test.js` or `.spec.js` as a test file. So, if you have a file called `divide.js`, you can put a `divide.test.js` next to it in the same directory and Jest will pick it up when it runs.
