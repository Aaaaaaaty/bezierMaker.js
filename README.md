# bezierMaker.js
Native HTML5 canvas can only support bezier curves up to third order. 

**bezierMaker.js supports the formation of arbitrary order of bezier curves in theory. And provide a [playground](https://aaaaaaaty.github.io/bezierMaker.js/playground/playground.html) on which can add and move control points, and generate draw animation.**
## Features
- [x] There can be arbitrary number of control points in playground.
- [x] The playground can show the display of the formation of curves.
- [x] Control points can be moved freely. 
- [x] The playground can show the tangent of the formation of bezier curves.
- [x] The formations of the less than or equal to third order bezier curves are based on the native API. 

## ScreenShots
![2017-12-28 17_21_52](https://user-images.githubusercontent.com/15126694/34406374-a5ebec54-ebf3-11e7-8a60-705261c7d0e4.gif)
![2017-12-28 17_38_06](https://user-images.githubusercontent.com/15126694/34406896-71c66528-ebf6-11e7-8aa0-7dcd16ef189e.gif)

[playground website](https://aaaaaaaty.github.io/bezierMaker.js/playground/playground.html)
## Usage
### Preparation
```
<script src="./bezierMaker.js"></script>
```
### Get Started
```
/**
 * canvas canvas's dom object
 * bezierCtrlNodesArr control point's array
 * color curve's color
 */
var canvas = document.getElementById('canvas')
//The formations of the less than or equal to third order bezier curves are based on the native API. 
var arr0 = [{x:70,y:25},{x:24,y:51}]
var arr1 = [{x:233,y:225},{x:170,y:279},{x:240,y:51}]
var arr2 = [{x:23,y:225},{x:70,y:79},{x:40,y:51},{x:300, y:44}]
var arr3 = [{x:333,y:15},{x:70,y:79},{x:40,y:551},{x:170,y:279},{x:17,y:239}]
var arr4 = [{x:53,y:85},{x:170,y:279},{x:240,y:551},{x:70,y:79},{x:40,y:551},{x:170,y:279}]
var bezier0 = new BezierMaker(canvas, arr0, 'black')
var bezier1 = new BezierMaker(canvas, arr1, 'red')
var bezier2 = new BezierMaker(canvas, arr2, 'blue')
var bezier3 = new BezierMaker(canvas, arr3, 'yellow')
var bezier4 = new BezierMaker(canvas, arr4, 'green')
bezier0.drawBezier()
bezier1.drawBezier()
bezier2.drawBezier()
bezier3.drawBezier()
bezier4.drawBezier()
```
### Effect
![image](https://user-images.githubusercontent.com/15126694/34406670-50cf6e10-ebf5-11e7-9299-9cfb983e5f78.png)

You can not know the exact position of the control point of the curve you want when drawing a complex higher order Bezier curve. 
When simulate in playground, we can get the coordinates of the control point in real time. Then we can make the coordinates into an array of objects and pass it into ```BezierMaker``` class to get the target curve.
## License
```
Copyright (C) 2017 2103887953@qq.com

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```