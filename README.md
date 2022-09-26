# bug-repo
Minimal Gatsby install for solving Gatsby/yoga-layout-prebuilt error on FreeBSD 13.1

Gatsby install with no errors on Freebsd 13.1.
However when `npm run develop` is run the following error message is emitted:

```
$ cd bug-repo
$ npm run develop

> bug-repo@1.0.0 develop
> gatsby develop

/home/settler/bug-repo/node_modules/yoga-layout-prebuilt/yoga-layout/build/Release/nbind.js:53
        throw ex;
        ^

Error: Cannot find module './artifacts/index.freebsd-x64.node'
Require stack:
- /home/settler/bug-repo/node_modules/@parcel/source-map/parcel_sourcemap_node/index.js
- /home/settler/bug-repo/node_modules/@parcel/source-map/dist/node.js
- /home/settler/bug-repo/node_modules/@parcel/utils/lib/index.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/public/Config.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/utils.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/public/Environment.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/public/Asset.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/Parcel.js
- /home/settler/bug-repo/node_modules/@parcel/core/lib/index.js
- /home/settler/bug-repo/node_modules/gatsby/dist/utils/parcel/compile-gatsby-files.js
- /home/settler/bug-repo/node_modules/gatsby/dist/bootstrap/get-config-file.js
- /home/settler/bug-repo/node_modules/gatsby/dist/bootstrap/load-config/index.js
- /home/settler/bug-repo/node_modules/gatsby/dist/services/initialize.js
- /home/settler/bug-repo/node_modules/gatsby/dist/services/index.js
- /home/settler/bug-repo/node_modules/gatsby/dist/state-machines/develop/services.js
- /home/settler/bug-repo/node_modules/gatsby/dist/state-machines/develop/index.js
- /home/settler/bug-repo/node_modules/gatsby/dist/commands/develop-process.js
- /home/settler/bug-repo/.cache/tmp-27117-jVSuU3O916Nw
    at Function.Module._resolveFilename (node:internal/modules/cjs/loader:956:15)
    at Function.Module._load (node:internal/modules/cjs/loader:804:27)
    at Module.require (node:internal/modules/cjs/loader:1022:19)
    at require (node:internal/modules/cjs/helpers:102:18)
    at Object.<anonymous> (/home/settler/bug-repo/node_modules/@parcel/source-map/parcel_sourcemap_node/index.js:15:18)
    at Module._compile (node:internal/modules/cjs/loader:1120:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1174:10)
    at Module.load (node:internal/modules/cjs/loader:998:32)
    at Function.Module._load (node:internal/modules/cjs/loader:839:12)
    at Module.require (node:internal/modules/cjs/loader:1022:19)
    at require (node:internal/modules/cjs/helpers:102:18)
    at Object.<anonymous> (/home/settler/bug-repo/node_modules/@parcel/source-map/dist/node.js:14:18)
    at Module._compile (node:internal/modules/cjs/loader:1120:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1174:10)
    at Module.load (node:internal/modules/cjs/loader:998:32)
    at Function.Module._load (node:internal/modules/cjs/loader:839:12) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    '/home/settler/bug-repo/node_modules/@parcel/source-map/parcel_sourcemap_node/index.js',
    '/home/settler/bug-repo/node_modules/@parcel/source-map/dist/node.js',
    '/home/settler/bug-repo/node_modules/@parcel/utils/lib/index.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/public/Config.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/utils.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/public/Environment.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/public/Asset.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/Parcel.js',
    '/home/settler/bug-repo/node_modules/@parcel/core/lib/index.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/utils/parcel/compile-gatsby-files.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/bootstrap/get-config-file.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/bootstrap/load-config/index.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/services/initialize.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/services/index.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/state-machines/develop/services.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/state-machines/develop/index.js',
    '/home/settler/bug-repo/node_modules/gatsby/dist/commands/develop-process.js',
    '/home/settler/bug-repo/.cache/tmp-27117-jVSuU3O916Nw'
  ]
}
```
