# bezierMaker.js
原生HTML5的canvas中所支持的贝塞尔曲线最多只到3阶。bezierMaker.js可以理论支持N阶贝塞尔曲线的生成，同时提供了[试验场](https://aaaaaaaty.github.io/bezierMaker.js/playground/playground.html)来自行添加拖拽控制点并形成绘制动画。


## Features
- [x] 试验场可添加任意数量控制点
- [x] 试验场支持展示曲线绘制的形成动画
- [x] 控制点可自由拖拽
- [x] 支持显示贝塞尔曲线形成过程的切线
- [x] 3阶及以下贝塞尔曲线的绘制采用原生API

## ScreenShots
![2017-12-28 17_21_52](https://user-images.githubusercontent.com/15126694/34406374-a5ebec54-ebf3-11e7-8a60-705261c7d0e4.gif)
![2017-12-28 17_38_06](https://user-images.githubusercontent.com/15126694/34406896-71c66528-ebf6-11e7-8aa0-7dcd16ef189e.gif)
[试验场传送门](https://aaaaaaaty.github.io/bezierMaker.js/playground/playground.html)
## Usage
```
/**
 * canvas canvas的dom对象
 * bezierCtrlNodesArr 控制点数组，包含x，y坐标
 * color 曲线颜色
 */
var canvas = document.getElementById('canvas')
//3阶之前采用原生方法实现
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

在绘制复杂的高阶贝塞尔曲线时无法知道每个控制点的精确位置可以在试验场中进行模拟，将得到的点坐标变为对象数组传递进```BezierMaker```类即可。

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