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
You can get the corresponding CDN link from [unpkg](https://unpkg.com/rverify/) or [jsdelivr](https://cdn.jsdelivr.net/gh/zpfz/RVerify.js/dist/).

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
Default: `#4E6EF2`

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
    'https://rverify.vercel.app/assets/1.jpg',
    'https://rverify.vercel.app/assets/2.jpg',
    'https://rverify.vercel.app/assets/3.jpg',
    'https://rverify.vercel.app/assets/4.jpg',
    'https://rverify.vercel.app/assets/5.jpg',
    'https://rverify.vercel.app/assets/6.jpg',
    'https://rverify.vercel.app/assets/7.jpg',
    'https://rverify.vercel.app/assets/8.jpg',
    'https://rverify.vercel.app/assets/9.jpg',
    'https://rverify.vercel.app/assets/10.jpg'
  ]
})
```
**NOTE**: A `152*152` px image needs to be set at least.

## Contributors
This project exists thanks to all the people who contribute.

![Feng L.H.](https://avatars2.githubusercontent.com/u/49757965?s=60&v=4) ![Guojun Chen](https://avatars2.githubusercontent.com/u/10856371?s=60&v=4) ![WampyCakes](https://avatars2.githubusercontent.com/u/9156604?s=60&v=4) 


## License
RVerify © 2020-present, Feng L.H. Released under the [MIT License](https://mit-license.org/).