<h1 align="center">RVerify.js</h1>
<div align="center">

✅❎ A lightweight image rotation verification plugin.

![Build](https://img.shields.io/badge/build-passing-brightgreen?style=flat-square) ![Downloads](https://img.shields.io/npm/dt/rverify?style=flat-square&color=red) ![Version](https://img.shields.io/github/package-json/v/zpfz/RVerify.js?style=flat-square&color=orange) ![License](https://img.shields.io/github/license/zpfz/RVerify.js?style=flat-square&color=blue)

</div>

## Installation
Add `RVerify.js` and `RVerify.css` to your project.
```js 
<script src="RVerify.js"></script>
<link rel="stylesheet" href="RVerify.css"/>
```
You can get the corresponding CDN link from [unpkg](https://unpkg.com/rverify/).

RVerify.js is available via [npm](https://www.npmjs.com/package/rverify).
```sh
npm install --save rverify
```

## Basic usage
Simply call `action()` to activate the verification modal.
```js
RVerify.action(function(res){
  console.log(res);
});
```
`res` will return 3 different codes:

- `0`: Verify failed.
- `1`: Verify successful.
- `2`: No action.(Return the code when the modal is closed before it successfully verified.)

## Configuration
You can configure some parameters through `RVerify.configure({})`.

### mask
Type: `Number` 
Default: `0.5`

Set the mask transparency.
```js
RVerify.configure({
  mask: 0.5
})
```

### maskClosable
Type: `Boolean` 
Default: `false`

Set whether click the mask can be closed.
```js
RVerify.configure({
  maskClosable: true
})
```
### closeIcon
Type: `String` 
Default: `(SVG CODE)`

Set the modal close icon.
```js
RVerify.configure({
  closeIcon: '(Please copy the SVG code)'
})
```
**NOTE**: It's recommended to set the SVG icon `width` and `height` to `20px`.

### sliderIcon
Type: `String` 
Default: `(SVG CODE)`

Set the modal slider icon.
```js
RVerify.configure({
  sliderIcon: '(Please copy the SVG code)'
})
```
**NOTE**: It's recommended to set the SVG icon `width` and `height` to `20px`.

### extraIcon
Type: `String` 
Default: `(SVG CODE)`

Set the modal extra icon.
```js
RVerify.configure({
  extraIcon: '(Please copy the SVG code)'
})
```
**NOTE**: It's recommended to set the SVG icon `width` and `height` to `15px`.

### tolerance
Type: `Number` 
Default: `10`

Set the verification tolerance range.(Range: 5°~45°)
```js
RVerify.configure({
  tolerance: 10
})
```
**NOTE**: In order to ensure a friendly verification effect, its value ranges from 5° to 45°.

### duration
Type: `Number` 
Default: `500`

Set the modal delay closing time.(Unit: ms)
```js
RVerify.configure({
  duration: 1000
})
```

### title
Type: `String` 
Default: `身份验证`

Set the modal title.
```js
RVerify.configure({
  title: 'Authentication'
})
```

### text
Type: `String` 
Default: `拖动滑块，使图片角度为正`

Set the modal text. 
```js
RVerify.configure({
  text: 'Drag the slider to make the image angle positive.'
})
```

### extra
Type: `String` 
Default: `null`

Set extra features at the bottom of the modal.
```js
RVerify.configure({
  extra: 'View on Npm'
})
```

### extraColor
Type: `String` 
Default: `#38F`

Set extra features text color at the bottom of the modal.
```js
RVerify.configure({
  extraColor: '#1ca280'
})
```

### extraLink
Type: `String` 
Default: `https://github.com/zpfz`

Set extra features link at the bottom of the modal.
```js
RVerify.configure({
  extraLink: 'https://www.npmjs.com/package/rverify'
})
```

### zIndex
Type: `Number` 
Default: `9999`

Set the modal z-index.
```js
RVerify.configure({
  zIndex: 1000
})
```

### album
Type: `Array` 
Default: `[]`

Set the modal randomly displayed image album.
```js
RVerify.configure({
  album: [
    'https://www.humanewatch.org/app/uploads/2018/10/Elephant_zoo.jpg',
    'https://askabiologist.asu.edu/sites/default/files/styles/panopoly_image_full/public/side-content/tortoiseshell_she-cat.jpg?itok=tbXBe5H7',
    'http://www.caraphil.org/mainsite/wp-content/uploads/2016/01/Monching-CARA-rescued-cat-pet-for-adoption-animal-welfare-in-the-Philippines.jpg'
  ]
})
```
**NOTE**: One image needs to be set at least.

## Thanks
RVerify © 2020-present, Feng L.H. Released under the [MIT License](https://mit-license.org/).