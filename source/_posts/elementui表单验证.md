---
title: element-ui 表单验证
type: article
tag: Element UI
abbrlink: 1103307926
date: 2020-10-17 00:00:00
---

## element-ui 表单验证
```js
data(){
	return {
		var passwordValidate = (rule,value,callback)=>{
			let reg = '正则'
			if(!reg.test(value)){
				callback(new Error('xxxx'))
			}
			callback() // 必须要加
		}
		formData:{
			username:'',
			user:{
				password:'' // 多层嵌套
			}
		}
		rule:{
			username:[
				{required:true,message:'必填',trigger:'blur'},
				{min:2,max:5,message:'2-5位',trigger:'blur'}
				{required:true,message:'xxx'，pattern:/正则/,trigger:'blur'}
			],
			'user.password':[
				{required:true,message:'必填',trigger:'blur'},
				{validator:passwordValidate，trigger:'blur'}
			]
		}
	}
}
```
### 表单提交验证

```js
submitForm(){
	this.$ref['formName'].validate(valid)=>{
		if(valid){
			// 提交成功时触发
		}else{
			// 提交失败时触发
			return false
		}
	}
}
```

