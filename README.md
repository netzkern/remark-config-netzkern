# 🐱 remark-preset-lint-netzkern

> This package provides netzkern .remarkrc as an extensible shared config.

-   Extends [`remark-preset-lint-recommended`](https://github.com/wooorm/remark-lint/tree/master/packages/remark-preset-lint-recommended).
-   Extends [`remark-preset-lint-consistent`](https://github.com/wooorm/remark-lint/tree/master/packages/remark-preset-lint-consistent).

## What is remark?

remark-lint is a markdown code style linter. Another linter? Yes. Ensuring the markdown you (and contributors) write is of great quality will provide better rendering in all the different markdown parsers, and makes sure less refactoring is needed afterwards.

## Install

npm:

```sh
npm install remark-config-netzkern --save
```

## Usage

You probably want to use it on the CLI through a config file:

```diff
 ...
 "remarkConfig": {
+  "plugins": ["preset-lint-netzkern"]
 }
 ...
```

Or use it on the CLI directly

```sh
remark -u preset-lint-netzkern readme.md
```

Or use this on the API:

```diff
 var remark = require('remark');
 var report = require('vfile-reporter');

 remark()
+  .use(require('remark-preset-lint-netzkern'))
   .process('_Emphasis_ and **importance**', function (err, file) {
     console.error(report(err || file));
   });
```

## Improving this config

[rules](https://github.com/wooorm/remark-lint/blob/master/doc/rules.md) lists all available official rules.
