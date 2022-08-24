# Sample project to reproduce ESM issue for `@solana/spl-token@0.3.2`

```sh
npm i
npm run build
node .
```

You'll see the following error:

```
/Users/rfeng/Projects/sandbox/spl-test/dist/index.js:3
var spl_token_1 = require("@solana/spl-token");
                  ^

Error [ERR_REQUIRE_ESM]: require() of ES Module /Users/rfeng/Projects/sandbox/spl-test/node_modules/@solana/spl-token/lib/cjs/index.js from /Users/rfeng/Projects/sandbox/spl-test/dist/index.js not supported.
/Users/rfeng/Projects/sandbox/spl-test/node_modules/@solana/spl-token/lib/cjs/index.js is treated as an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which declares all .js files in that package scope as ES modules.
Instead rename /Users/rfeng/Projects/sandbox/spl-test/node_modules/@solana/spl-token/lib/cjs/index.js to end in .cjs, change the requiring code to use dynamic import() which is available in all CommonJS modules, or change "type": "module" to "type": "commonjs" in /Users/rfeng/Projects/sandbox/spl-test/node_modules/@solana/spl-token/package.json to treat all .js files as CommonJS (using .mjs for all ES modules instead).

    at Object.<anonymous> (/Users/rfeng/Projects/sandbox/spl-test/dist/index.js:3:19) {
  code: 'ERR_REQUIRE_ESM'
```
