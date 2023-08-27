---
title: jQuery封装ajax的方法
type: article
tag: jQuery
abbrlink: 3855898246
date: 2020-05-02 00:00:00
---

# 1、$.get()
参数有4个，必填参数是url地址，其他参数都是选填参数，可以没有，参数的形式是对象形式。

```yaml
$.get({
    url : 地址(必填),
    data : 携带的参数，对象形式,
    dataType : 期望的数据类型，如果为json，会将会断返回的json串，自动解析,
    success : function(){
       	请求成功时执行的函数
    }
})
```
# 2、$.post()
参数有4个，必填参数是url地址，其他参数都是选填参数，可以没有，参数的形式是对象形式。
```yaml
$.post({
    url : 地址(必填),
    data : 携带的参数，对象形式,
    dataType : 期望的数据类型，如果为json，会将会断返回的json串，自动解析,
    success : function(){} 请求成功时执行的函数
})
```
# 3、$.ajax()
有n个参数，默认请求方式是 get 方式

```yaml
$.ajax({
	常用：
    url : 地址,
    type : 请求方式，默认值get方式,
    data : {} 传参参数，必须是对象形式,
    dataType : json , 设定为json，会自动解析反应体中的json串,
    success : function(){} 请求成功时执行的函数
    
    不常用：
    async : 设定是否异步,默认值是true,异步执行ajax请求
    error : function(){}  请求错误时执行的函数
                          请求成功时不会执行
    timeout : 设定时间,单位 毫秒
              如果请求时间超过设定的时间,认为是请求失败
              必须是异步执行
    cache : 设定是否缓存请求结果
            默认值是 true,缓存请求结果
            必须是get方式,这个设定才起作用
            post方式不会缓存,设定也没有效果
	context : 指定 执行函数中 this的指向
})
```
