# Videx npm template

Template for npm packages with testing and automatic documentation.

- **Compiler**: [Babel](https://www.npmjs.com/package/@babel/core)
- **Module bundler**: [Rollup](https://www.npmjs.com/package/rollup)
- **Testing**: [Jest](https://www.npmjs.com/package/jest)
- **Documentation**: [JSDoc](https://www.npmjs.com/package/jsdoc)
- **JSDoc template**: [Docdash](https://www.npmjs.com/package/docdash)

# TODO: Fix under

- [GitHub Repository](https://github.com/equinor/videx-math)
- [Documentation](https://equinor.github.io/videx-math)

## Installation
```js
npm install --save @equinor/videx-math
```

## Usage

```js
// ES6
import { clamp, lerp, ... } from '@equinor/videx-math';

// ObservableHQ
const someVar = require('@equinor/videx-math@X.X.X/dist/bundle.umd.js');
const lerp = someVar.lerp;
```
Where X.X.X is desired version number.

## Available functions

<table style="width:auto;">
  <tr>
    <td><a href="https://equinor.github.io/videx-math/global.html#clamp">clamp</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#degrees">degrees</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#lerp">lerp</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#nrad">nrad</a></td>
  </tr>
  <tr>
    <td><a href="https://equinor.github.io/videx-math/global.html#radians">radians</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#round">round</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#seq">seq</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#seqI">seqI</a></td>
  </tr>
  <tr>
    <td><a href="https://equinor.github.io/videx-math/global.html#smoothstep">smoothstep</a></td>
    <td><a href="https://equinor.github.io/videx-math/global.html#step">step</a></td>
  </tr>
</table>

<br/>

![Equinor Logo](images/equinor-logo.png)
