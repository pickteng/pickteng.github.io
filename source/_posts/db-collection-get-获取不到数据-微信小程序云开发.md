---
title: db.collection.get()获取不到数据---微信小程序云开发
date: 2020-07-02 15:29:07
tags: 微信小程序
---

#### 代码：
```js
// 从in_theaters云数据库里获取三条数据
let res = await db.collection("in_theaters").where({}).limit(3).get()
console.log('res=>',res)
```
#### 运行结果：获取不到数据库数据
![图片](2020070211561671.png)

#### **解决**：修改数据库权限
![图片](20200702115807699.png)
#### 改完权限之后运行：成功拿到
![图片](20200702115929564.png)
