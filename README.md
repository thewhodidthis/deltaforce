## about

Simplifies mouse tracking keeping in mind that `PointerEvent.movementX/Y` might be the more obvious way to go in the near future.

## setup

Load via script tag:

```html
<!-- Just an IIFE namespaced `deltaforce` -->
<script src="https://thewhodidthis.github.io/deltaforce/deltaforce.js"></script>
```

Source from an import map:

```json
{
  "imports": {
    "deltaforce": "https://thewhodidthis.github.io/deltaforce/main.js"
  }
}
```

Download from GitHub directly if using a package manager:

```sh
# Add to package.json
npm install thewhodidthis/deltaforce
```

## usage

Initialize with a DOM selector, then call repeatedly for delta values in the form of `{ x, y, z, state }` as for example,

```js
import tracker from "deltaforce"

const update = tracker(/* Some element, document by default */)

setInterval(() => {
  console.table(update())
}, 1000)
```
