# poc-camanjs

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# PROBLEMS
## BUILD FAILURE

when you try to load caman like the following,

```index.js
import Caman from 'caman';
```

an error occurs.

```
error  in ./node_modules/canvas/build/Release/canvas.node

Module parse failed: Unexpected character '�' (1:0)
You may need an appropriate loader to handle this file type.
(Source code omitted for this binary file)

 @ ./node_modules/canvas/lib/bindings.js 3:17-56
 @ ./node_modules/canvas/lib/canvas.js
 @ ./node_modules/caman/dist/caman.full.js
 @ ./src/router/index.js
 @ ./src/main.js
 @ multi (webpack)-dev-server/client?http://localhost:8080 webpack/hot/dev-server ./src/main.js
```

To avoid this error, read caman lib by `<script>` tag.


