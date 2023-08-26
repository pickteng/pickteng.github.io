---
title: css3立方体
date: 2020-02-22
tag: CSS
---

# 用到的属性
## hover
作用：当鼠标移入时产生定义的hover样式
使用方法：例：div标签&nbsp; &nbsp; &nbsp; div:hover{样式}
## transform
作用：对元素进行移动、旋转、缩放、倾斜
|值|描述  |
|--|--|
|translate(x,y)  |  2D 移动 (单位px) |
|translate3d(x,y,z)  |  3D 移动 |
|translateX(x) |  X轴移动 |
|translateY(y) |  Y轴移动 |
| scale(x) |  2D 缩放  |
|scale3d(x,y,z)  |  3D 缩放 |
|scaleX(x)  |  沿X轴缩放 |
|scaleY(y)  |  沿Y轴缩放 |
|scaleZ(z) |  沿Z轴缩放 |
|rotate(angle)  |  2D 旋转 (单位deg) |
|rotate3d(x,y,z,angle) |  3D 旋转 |
|rotateX(angle) |  沿X轴旋转 |
|rotateY(angle) |  沿Y轴旋转 |
|rotateZ(angle) |  沿Z轴旋转 |
|skew(x-angle,y-angle)  |  沿着 X 和 Y 轴的 2D 倾斜 (单位deg) |
|skewX(angle)|  沿着 X 轴的 2D 倾斜 |
|skewX(angle) |  沿着 Y 轴的 2D 倾斜 |
注：skew没有3D效果
## transition
|值|描述  |
|--|--|
| transition-property |指定CSS属性的name，transition效果  |
| transition-duration | transition效果需要指定多少秒或毫秒才能完成 |
| transition-timing-function | 指定transition效果的速度曲线 |
| transition-delay | 	定义transition效果延迟的时间 |
复合写法：transition: property duration timing-function delay;
## perspective（景深(3D眼镜)）
语法：perspective: number|none; （单位px）
|值|描述  |
|--|--|
| number | 元素距离视图的距离 |
| none| 默认值。与 0 相同。不设置透视 |

注：perspective 属性只影响 3D 转换元素
## transform-style
语法：transform-style: flat|preserve-3d;
|值|描述  |
|--|--|
| flat | 表示所有子元素在2D平面呈现 |
| preserve-3d| 表示所有子元素在3D空间中呈现（创建3D空间） |

## backface-visibility
语法：backface-visibility: visible|hidden;
|值|描述  |
|--|--|
| visible |背面可见  |
| hidden|背面不可见  |

# 代码解析
## html部分

```html
<div class="box">
	<ul>
		<li>上</li>
		<li>下</li>
		<li>左</li>
		<li>右</li>
		<li>前</li>
		<li>后</li>
	</ul>
</div>
```

## css部分

```css
<style type="text/css">
	/* 去掉默认样式 */
	*{margin: 0;padding: 0;}
	ul li{list-style: none;}
	
	.box {
		width: 600px; 
		height: 600px; 
		background: #eee;
		margin: 0 auto;
		position: relative;
		perspective: 800px; /* 景深 */
	.box ul{
		width: 300px; 
		height: 300px; 
		position: absolute;
		top: 0; 
		bottom: 0; 
		left: 0; 
		right: 0; 
		margin: auto; 
		transform-style: preserve-3d; /* 创建3D空间 */
		transition: all 4s;}
	.box ul:hover{
		transform: rotateX(360deg) rotateY(360deg);
	}
	.box ul li{
		width: 300px;
		height: 300px; 
		text-align: center; 
		line-height: 300px; 
		font-size: 48px; 
		position: absolute;
		backface-visibility: hidden; /* 设置背面不可见 */ }
	.box ul li:nth-child(1) {background: rgba(255,0,0,.5); transform: translateY(-150px) rotateX(90deg);}
	.box ul li:nth-child(2) {background: rgba(0,255,0,.5); transform: translateY(150px) rotateX(-90deg);}
	.box ul li:nth-child(3) {background: rgba(0,0,255,.5); transform: translateX(-150px) rotateY(-90deg);}
	.box ul li:nth-child(4) {background: rgba(255,0,255,.5); transform: translateX(150px) rotateY(90deg);}
	.box ul li:nth-child(5) {background: rgba(255,255,0,.5); transform: translateZ(150px);}
	.box ul li:nth-child(6) {background: rgba(0,255,255,.5); transform: translateZ(-150px) rotateY(180deg); }		
</style>
```



