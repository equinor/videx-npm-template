# Videx npm template

Template for npm packages with testing and automatic documentation.

- **Compiler**: [Babel](https://www.npmjs.com/package/@babel/core)
- **Module bundler**: [Rollup](https://www.npmjs.com/package/rollup)
- **Testing**: [Jest](https://www.npmjs.com/package/jest)
- **Documentation**: [JSDoc](https://www.npmjs.com/package/jsdoc)
- **JSDoc template**: [Docdash](https://www.npmjs.com/package/docdash)

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

### Create package

The entry point for the actual npm package is defined as 'src/index.js'. This can be changed within 'rollup.config.js'.
All public variables, functions and classes should be exported within this file.

## Sample function

<table style="width:auto;">
  <tr>
    <td><a href="https://equinor.github.io/videx-math/global.html#clamp">hello</a></td>
  </tr>
</table>

<br/>

![Equinor Logo](images/equinor-logo.png)
