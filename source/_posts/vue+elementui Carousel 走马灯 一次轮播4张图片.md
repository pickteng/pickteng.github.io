---
title: vue+elementui Carousel 走马灯 一次轮播4张图片
tag: Element
type: article
abbrlink: 2360078537
date: 2021-08-19 00:00:00
---

## vue
```html
<el-carousel :loop="false" :autoplay="false" height="204px">
    <el-carousel-item class="el-car-item" v-for="(list, index) in dataList" :key="index">
       <img v-for="(imgList,index2) in list" :key="index2" class="top-img" :src="imgList.img" :alt="imgList.title" />
    </el-carousel-item>
</el-carousel>
```
## 后端返回数据

```js
dataList: [
        {
          "title": "111",
          "url": "xxx",
          "img": "xxx"
        },
        {
          "title": "222",
          "url": "xxx",
          "img": "xxx"
        },
        {
          "title": "333",
          "url": "xxx",
          "img": "xxx"
        },
        {
          "title": "444",
          "url": "xxx",
          "img": "xxx"
        },
        {
          "title": "555",
          "url": "xxx",
          "img": "xxx"
        },
        {
          "title": "666",
          "url": "xxx",
          "img": "xxx"
        },
      ]
```
## 处理后端返回的数据
```js
	let newDataList = []
    let current = 0
    if(this.dataList && this.dataList.length>0){
      for(let i=0;i<=this.dataList.length-1;i++){
        if(i%4 !== 0 || i === 0 ){
          if(!newDataList[current]){
            newDataList.push([this.dataList[i]])
          }else{
            newDataList[current].push(this.dataList[i])
          }
        }else{
          current++
          newDataList.push([this.dataList[i]])
        }
      }
    }
    this.dataList = [...newDataList]
```
## css

```css
.el-car-item {
    width: 100%;
    display: flex;
    .top-img{
      width: 284px;
      height: 184px;
      margin-right: 20px;
      cursor: pointer;
    }
  }
```

