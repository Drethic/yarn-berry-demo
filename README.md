# Setup Steps
1. Run `yarn install` in the root directory
2. Run `yarn pnpify --sdk vscode` to install the sdks
3. Run `yarn install` in the lib directory
4. Run `yarn dev` in the lib directory

You should receive the following error message when you run `yarn dev`:
```
Internal Error: Unable to locate pnpapi, the module '/Projects/demo/lib/.pnp.js' is controlled by multiple pnpapi instances.
This is usually caused by using the global cache (enableGlobalCache: true)

Controlled by:
  /Projects/demo/lib/.pnp.js
  /Projects/demo/.pnp.js
This is usually caused by using the global cache (enableGlobalCache: true)

Controlled by:
  /Projects/demo/lib/.pnp.js
  /Projects/demo/.pnp.js
    at Object.findApiPathFor (/Projects/demo/lib/.pnp.js:29343:13)
    at Function.external_module_.Module._resolveFilename (/Projects/demo/lib/.pnp.js:28315:182)
    at Function.external_module_.Module._load (/Projects/demo/lib/.pnp.js:28204:48)
    at Module.require (internal/modules/cjs/loader.js:903:19)
    at require (internal/modules/cjs/helpers.js:74:18)
    at S (/Projects/demo/.yarn/releases/yarn-2.4.0.cjs:2:418340)
    at Module.k (/Projects/demo/.yarn/releases/yarn-2.4.0.cjs:2:418445)
    at S.findPackageLocation (/Projects/demo/.yarn/releases/yarn-2.4.0.cjs:2:265281)
    at /Projects/demo/.yarn/releases/yarn-2.4.0.cjs:2:425060
    at Function.openPromise (/Projects/demo/.yarn/releases/yarn-2.4.0.cjs:2:489248)
```

