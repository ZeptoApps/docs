Many of our client using "Minimog" theme where our hidden products are visible in the product recommendation section.
This theme uses custom JS to generate the product recommendation, so we can not use our liquid code inside the loop.

### Steps:

- Go to `theme.liquid` file and search for `app.min.js` and change it to `app.js` (sometime this file can be found inside `script-tags.liquid` file).
- Now go to `ASSEST` folder and open the `app.js` file.
- Comment the default code and use the following code, view this [screenshot](https://drive.google.com/file/d/1XYtOE3KvmbB_OZCWIW1eV-Vc_rzVditA/view?usp=sharing) to see the line number.

**Use the following code:**

```js
this.productHandles = [];
products.forEach((_ref) => {
  if (_ref.type !== "PPLR_HIDDEN_PRODUCT")
    this.productHandles.push(_ref.handle);
});
```

**The code you will need to comment out:**

```js
this.productHandles = products.map((_ref) => {
  let { handle } = _ref;
  return handle;
});
```
