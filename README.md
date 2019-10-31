# Videx npm template

Template for npm packages with testing and automatic documentation.

- **Compiler**: [Babel](https://www.npmjs.com/package/@babel/core)
- **Module bundler**: [Rollup](https://www.npmjs.com/package/rollup)
- **Testing**: [Jest](https://www.npmjs.com/package/jest)
- **Documentation**: [JSDoc](https://www.npmjs.com/package/jsdoc)
- **JSDoc template**: [Docdash](https://www.npmjs.com/package/docdash)
- **Code compressor**: [Terser](https://www.npmjs.com/package/terser)

## Repository

- [GitHub](https://github.com/equinor/videx-npm-template)

## Setup guide

### Cloning repository

Start by cloning the template repository to desired directory.

```
git clone https://github.com/equinor/videx-npm-template.git
```

### Modify package.json

Fields that need to be modified are:

- **name**: The name of the npm package.
- **description**: The description of the npm package.
- **repository.url**: Should point to the GitHub repository.
- **keywords**: Keywords to make it easier to find the package on npm.
- **author**: Package author. For multiple authors, consider using '[contributors](https://docs.npmjs.com/files/package.json#people-fields-author-contributors)'.
- **bugs.url**: Should point to "GitHub repository"/issues.
- **homepage**: Could point to "GitHub repository"#readme.

### Install dependencies

Install all dev dependencies defined in package.json using node.

```
npm install
```

## Usage

### Creating package

The entry point for the actual npm package is defined as 'src/index.js'. This can be changed within 'rollup.config.js'.
Any public variables, functions and classes should be exported within this file.

**Important**: Default values on input parameters are strongly discouraged. Babel compilation integrates these variables into the functions themselves, which breaks documentation and IntelliSense.

Example of how default values can be avoided:

#### Before

```js
export function hello(name = 'npm') {
  return `Hello ${name}!`;
}
```

#### After

```js
export function hello(name) {
  if (name === undefined) name = 'npm';
  return `Hello ${name}!`;
}
```

Optional parameters should be documented!

```js
/**
 * ...
 * @param {String} [name='npm'] Name to greet (Default: 'npm')
 * ...
 */
```

### Document generation

```
npm run docs
```

Three part process:

1. Deletes the docs-folder, if it exists.
2. Automatically generates documentation to a new docs-folder.
3. Copies the images-folder into docs.

The copying of images makes it possible to refer to local images within the README!

### Creating tests

All tests are defined within the test-folder. Jest naming convention is to place tests for SOMESCRIPT.js in a single file SOMESCRIPT.test.js.

### Testing

```
npm run test
```

Executes all tests defined within the test folder.

```
npm run test:watch
```

Executes all tests, but does not return immediately. Makes it possible to re-run failed tests quickly.

### Building/Compiling

```
npm run build
```

Compiles the code found within the src-folder. Build is outputted to a new dist-folder.

### Publication

```
npm run pub
```

Attemps to publish the package to npm. As part of the publishing process, the source code is re-compiled.

## Publish documentation

GitHub pages is used to show documentation. To set up GitHub pages, start by navigating to the settings tab within the GitHub repository.

![Settings Tab](images/settings-tab.png)

Scroll down and set GitHub pages source to the docs-folder of the master branch.

![Settings Tab](images/github-pages.png)

Publishing the documentation will produce a link. This link can be included in the README for easy navigation.

![Settings Tab](images/github-pages-published.png)

Sample documentation can be found [here](https://equinor.github.io/videx-npm-template/).

## Sample function

<table style="width:auto;">
  <tr>
    <td><a href="https://equinor.github.io/videx-npm-template/global.html#hello">hello</a></td>
  </tr>
</table>

<br/>

![Equinor Logo](images/equinor-logo.png)
