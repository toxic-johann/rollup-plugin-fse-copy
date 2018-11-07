# rollup-plugin-copy

[![Greenkeeper badge](https://badges.greenkeeper.io/toxic-johann/rollup-plugin-fse-copy.svg)](https://greenkeeper.io/)

Forked from https://github.com/meuter/rollup-plugin-copy. Published as a backup.

*Very* basic rollup plugin to copy static assets over to you public directory. Files are copied using [fs-extra.copy](https://github.com/jprichardson/node-fs-extra/blob/master/docs/copy.md) 

## Installation

This package can be installed using npm:

```
npm install rollup-plugin-copy
```

## Usage

Add the following lines to your `rollup.config.js`:

```javascript
import copy from 'rollup-plugin-copy';

...

export default {
    ...
    plugins: [
        ...
        copy({
            "src/index.html": "dist/index.html",
            "node_modules/bootstrap/dist": "dist/vendor/bootstrap",
            "node_modules/font-awesome": "dist/vendor/font-awesome",
            "src/main.html": [ "dist/main.html", "lib/main.html" ],
            verbose: true
        })
        ...
    ]
    ...
}
```

## Options

* `verbose`: `<boolean>` : display verbose message  (default is `false`)

![verbose](verbose.png)

