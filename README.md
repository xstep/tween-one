# rc-tween-one
---

React TweenOne Component


[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][coveralls-image]][coveralls-url]
[![gemnasium deps][gemnasium-image]][gemnasium-url]
[![node version][node-image]][node-url]
[![npm download][download-image]][download-url]

[npm-image]: http://img.shields.io/npm/v/rc-tween-one.svg?style=flat-square
[npm-url]: http://npmjs.org/package/rc-tween-one
[travis-image]: https://img.shields.io/travis/react-component/tween-one.svg?style=flat-square
[travis-url]: https://travis-ci.org/react-component/tween-one
[coveralls-image]: https://img.shields.io/coveralls/react-component/tween-one.svg?style=flat-square
[coveralls-url]: https://coveralls.io/r/react-component/tween-one?branch=master
[gemnasium-image]: http://img.shields.io/gemnasium/react-component/tween-one.svg?style=flat-square
[gemnasium-url]: https://gemnasium.com/react-component/tween-one
[node-image]: https://img.shields.io/badge/node.js-%3E=_0.10-green.svg?style=flat-square
[node-url]: http://nodejs.org/download/
[download-image]: https://img.shields.io/npm/dm/rc-tween-one.svg?style=flat-square
[download-url]: https://npmjs.org/package/rc-tween-one


## Browser Support

|![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)|
| --- | --- | --- | --- | --- |
| IE 8+ ✔ | Chrome 31.0+ ✔ | Firefox 31.0+ ✔ | Opera 30.0+ ✔ | Safari 7.0+ ✔ |

## Development

```
npm install
npm start
```

## Example

http://localhost:8100/examples/

http://react-component.github.io/tween-one/


## install


[![rc-tween-one](https://nodei.co/npm/rc-tween-one.png)](https://npmjs.org/package/rc-tween-one)


## Usage

```js
var TweenOne = require('rc-tween-one');
var React = require('react');
React.render(<TweenOne animation={{x:100}}>
               demo
             </TweenOne>, container);
```

## API

### props

| name      | type           | default | description    |
|------------|----------------|---------|----------------|
| animation  | object / array | null    | animate configure parameters |
| paused      | boolean        | false   | animate pause |
| reverse    | boolean        | false   | animate revers |
| onChange   | func           | null    | when the animation change called, callback({ moment, item, tween, index, mode}) |
| moment     | number         | null    | set the current frame    |
| component  | string         | `div`   | component tag  |


### animation = { }
> transform need to set the initial value, must be set in the style;

| name      | type           | default | description    |
|------------|----------------|---------|----------------|
| type       | string         | `to`    | play type: `to` `from`|
| in style   | string / number| null  | CSS style value: `translateX` `rotateX` `color` `marginTop` or gsap: `x` `y`... |
| duration   |  number        | 450     | animate duration     |
| delay      | number         | 0       | animate delay  |
| repeat     | number         | 0       | animate repeat, To repeat indefinitely, use  -1 |
| repeatDelay| number         | 0       | repeat start delay |
| yoyo       | boolean        | false   | if `true`, every other repeat cycle will run in the opposite direction so that the tween appears to go back and forth (forward then backward).  |
| ease       | string         | `easeInOutQuad` | animate ease |
| bezier     | object         | null    | bezier curve animate |
| onStart    | func           | null    | A function that should be called when the tween begins  |
| onUpdate   | func           | null    | A function that should be called every time the animate updates  |
| onComplete | func           | null    | A function that should be called when the animate has completed  |
| onRepeat   | func           | null    | A function that should be called each time the animate repeats  |



### animation =[ ] is timeline

### bezier = { }

| name      | type           | default | description    |
|------------|----------------|---------|----------------|
| type       | string         | `soft`  | `thru`, `soft`, `quadratic`, `cubic` |
| autoRotate | boolean        | false   | to automatically rotate the target according to its position on the Bezier path  |
| vars       | array          | null    | bezier point data，as: `{x:100,y:100}` |

> bezier API refer to [gsap BezierPlugin](http://greensock.com/docs/#/HTML5/GSAP/Plugins/BezierPlugin/)
