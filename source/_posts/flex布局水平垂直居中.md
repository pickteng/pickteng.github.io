---
title: flex布局
date: 2020-02-28
tag: CSS
---

### 排列方式为行（主轴为水平方向，侧轴为垂直方向）
1、给父元素添加弹性布局
	display: flex;
2、给父元素添加  justify-content 属性  （水平居中）
	  justify-content 属性决定了主轴方向上子项的对齐和分布方式
	    justify-content: center
3、给父元素添加 align-items 属性（垂直居中）
align-items : 每一行中的子元素上下对齐方式
align-items: center
总：父元素{ display: flex; justify-content: center; align-items: center;}
### 排列方式为列（主轴为垂直方向，侧轴为水平方向）
1、给父元素上添加弹性布局
	display: flex;
2、给父元素添加  justify-content 属性  （垂直居中）
	  justify-content 属性决定了主轴方向上子项的对齐和分布方式
	    justify-content: center
3、给父元素添加 align-items 属性（水平居中）
align-items : 每一行中的子元素上下对齐方式
align-items: center
总：父元素{ display: flex; justify-content: center; align-items: center;}


##### 默认情况下，排列方式为行。
例：
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style type="text/css">
			*{margin: 0; padding: 0;}
			ul{ list-style: none;}
			
			ul{ display: flex; justify-content: center; align-items: center; width: 300px; height: 100px; 
			margin: 100px auto; border: 1px solid pink;}
			ul li{ margin: 10px;}
		</style>
	</head>
	<body>
		<ul>
			<li>111</li>
			<li>222</li>
			<li>333</li>
			<li>444</li>
		</ul>
	</body>
</html>

```
效果图：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200228221306648.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3RjMTE0MzQ4MTk1Ng==,size_16,color_FFFFFF,t_70)
