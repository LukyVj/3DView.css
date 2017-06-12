# 3DView
https://lukyvj.github.io/3DView.css/


This project is an attempt to reproduce the (R.I.P) [Firefox's 3D Dom view](https://developer.mozilla.org/en/docs/Tools/3D_View) ( aka tilt 3D ) with CSS. 

-----

Using CSS transforms, outline and shadows, I tried to make it easier for everyone to understand how the elements on a webpage are organised.

|  Algolia.com  | CSS-Tricks.com  | Github.com   |
| ------------- | ------------- | ------------- |
| ![](https://puu.sh/whT8Y/1865c0ed65.png) | ![](https://puu.sh/whT9k/4e8ce90169.png)  | ![](https://puu.sh/whT9j/4c7cb07327.png)  |

## Usage
Load one of the three 3DView source files on your website:
```html
<link rel="stylesheet" src="path/to/3DView-left.css" />
```

And add the debug attribute to your `<html>` or `<body>` tag.
```html
<html debug="true">
```

### Sass
There is a Sass mixin that helps you making the maximum out of this technique :

```sass
[debug=true] {
  @include debugView(<deepness>, <property>)
}
```
| Name  | Description |
| ------------- | ------------- |
| &lt;deepness>  |  Numeric - Indentation deepness ( * > * > * [...] )  |
| &lt;property>  |  String - Property to offset ( left, margin-left, transform )  |



## Demo:
<details>
  <summary>Demo on Algolia.com</summary>
  <img src="demo.gif" />
</details>

## Bookmarklets
Add a new bookmark with one of this value as URL
3DView-left:
```
javascript:(function (){ let style = document.createElement('style'); style.innerHTML = '[debug=true] { outline: 1px solid lime; outline-offset: -1px; -webkit-transform-style: preserve-3d; transform-style: preserve-3d; -webkit-perspective: 600px; perspective: 600px; -webkit-transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); } [debug=true] * { outline: 1px solid lime; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:before, [debug=true] *:after { outline: 1px solid #0ff; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:after { outline-color: #f0f; } [debug=true] *:hover { outline-color: #f0f !important; outline-width: 2px !important; outline-style: dashed !important; } [debug=true] *:hover:before, [debug=true] *:hover:after { outline-color: #0ff !important; outline-width: 2px !important; } [debug=true] * { outline-color: rgba(45, 223, 171, 0.9) !important; left: 0.5vw !important; } [debug=true] * > * { outline-color: rgba(90, 144, 110, 0.9) !important; left: 1vw !important; } [debug=true] * > * > * { outline-color: rgba(145, 104, 79, 0.9) !important; left: 1.5vw !important; } [debug=true] * > * > * > * { outline-color: rgba(179, 72, 55, 0.9) !important; left: 2vw !important; } [debug=true] * > * > * > * > * { outline-color: rgba(205, 53, 40, 0.9) !important; left: 2.5vw !important; } [debug=true] * > * > * > * > * > * { outline-color: rgba(224, 44, 34, 0.9) !important; left: 3vw !important; } [debug=true] * > * > * > * > * > * > * { outline-color: rgba(233, 45, 39, 0.9) !important; left: 3.5vw !important; } [debug=true] * > * > * > * > * > * > * > * { outline-color: rgba(240, 52, 45, 0.9) !important; left: 4vw !important; } [debug=true] * > * > * > * > * > * > * > * > * { outline-color: rgba(243, 60, 56, 0.9) !important; left: 4.5vw !important; } [debug=true] * > * > * > * > * > * > * > * > * > * { outline-color: rgba(245, 72, 70, 0.9) !important; left: 5vw !important; }'; document.head.appendChild(style); document.body.setAttribute('debug','true'); })();
```

3DView-margin:
```
javascript:(function (){ let style = document.createElement('style'); style.innerHTML = '[debug=true] { outline: 1px solid lime; outline-offset: -1px; -webkit-transform-style: preserve-3d; transform-style: preserve-3d; -webkit-perspective: 600px; perspective: 600px; -webkit-transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); } [debug=true] * { outline: 1px solid lime; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:before, [debug=true] *:after { outline: 1px solid #0ff; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:after { outline-color: #f0f; } [debug=true] *:hover { outline-color: #f0f !important; outline-width: 2px !important; outline-style: dashed !important; } [debug=true] *:hover:before, [debug=true] *:hover:after { outline-color: #0ff !important; outline-width: 2px !important; } [debug=true] * { outline-color: rgba(45, 223, 171, 0.9) !important; margin-left: 0.5vw !important; } [debug=true] * > * { outline-color: rgba(90, 144, 110, 0.9) !important; margin-left: 1vw !important; } [debug=true] * > * > * { outline-color: rgba(145, 104, 79, 0.9) !important; margin-left: 1.5vw !important; } [debug=true] * > * > * > * { outline-color: rgba(179, 72, 55, 0.9) !important; margin-left: 2vw !important; } [debug=true] * > * > * > * > * { outline-color: rgba(205, 53, 40, 0.9) !important; margin-left: 2.5vw !important; } [debug=true] * > * > * > * > * > * { outline-color: rgba(224, 44, 34, 0.9) !important; margin-left: 3vw !important; } [debug=true] * > * > * > * > * > * > * { outline-color: rgba(233, 45, 39, 0.9) !important; margin-left: 3.5vw !important; } [debug=true] * > * > * > * > * > * > * > * { outline-color: rgba(240, 52, 45, 0.9) !important; margin-left: 4vw !important; } [debug=true] * > * > * > * > * > * > * > * > * { outline-color: rgba(243, 60, 56, 0.9) !important; margin-left: 4.5vw !important; } [debug=true] * > * > * > * > * > * > * > * > * > * { outline-color: rgba(245, 72, 70, 0.9) !important; margin-left: 5vw !important; }'; document.head.appendChild(style); document.body.setAttribute('debug','true'); })();
```

3DView-transform:
```
javascript:(function (){ let style = document.createElement('style'); style.innerHTML = '[debug=true] { outline: 1px solid lime; outline-offset: -1px; -webkit-transform-style: preserve-3d; transform-style: preserve-3d; -webkit-perspective: 600px; perspective: 600px; -webkit-transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); transform: rotateY(16deg) scale(0.9) translateX(5%) translateY(1%) skewY(-6deg); } [debug=true] * { outline: 1px solid lime; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:before, [debug=true] *:after { outline: 1px solid #0ff; outline-offset: -1px; box-shadow: 0 0 100px rgba(0, 0, 0, 0.15), -1px -1px 0 rgba(0, 0, 0, 0.1), -2px -2px 0 rgba(0, 0, 0, 0.1), -3px -3px 0 rgba(0, 0, 0, 0.1), -4px -4px 0 rgba(0, 0, 0, 0.1), -5px -5px 0 rgba(0, 0, 0, 0.1), -6px -6px 0 rgba(0, 0, 0, 0.1); } [debug=true] *:after { outline-color: #f0f; } [debug=true] *:hover { outline-color: #f0f !important; outline-width: 2px !important; outline-style: dashed !important; } [debug=true] *:hover:before, [debug=true] *:hover:after { outline-color: #0ff !important; outline-width: 2px !important; } [debug=true] * { outline-color: rgba(45, 223, 171, 0.9) !important; transform: translateX(0.25vw) !important; } [debug=true] * > * { outline-color: rgba(90, 144, 110, 0.9) !important; transform: translateX(0.5vw) !important; } [debug=true] * > * > * { outline-color: rgba(145, 104, 79, 0.9) !important; transform: translateX(0.75vw) !important; } [debug=true] * > * > * > * { outline-color: rgba(179, 72, 55, 0.9) !important; transform: translateX(1vw) !important; } [debug=true] * > * > * > * > * { outline-color: rgba(205, 53, 40, 0.9) !important; transform: translateX(1.25vw) !important; } [debug=true] * > * > * > * > * > * { outline-color: rgba(224, 44, 34, 0.9) !important; transform: translateX(1.5vw) !important; } [debug=true] * > * > * > * > * > * > * { outline-color: rgba(233, 45, 39, 0.9) !important; transform: translateX(1.75vw) !important; } [debug=true] * > * > * > * > * > * > * > * { outline-color: rgba(240, 52, 45, 0.9) !important; transform: translateX(2vw) !important; } [debug=true] * > * > * > * > * > * > * > * > * { outline-color: rgba(243, 60, 56, 0.9) !important; transform: translateX(2.25vw) !important; } [debug=true] * > * > * > * > * > * > * > * > * > * { outline-color: rgba(245, 72, 70, 0.9) !important; transform: translateX(2.5vw) !important; }'; document.head.appendChild(style); document.body.setAttribute('debug','true'); })();
```
