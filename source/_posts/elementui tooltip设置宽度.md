---
title: element-ui tooltip手动设置宽度
date: 2021-07-29
tag: Element UI
---

```
<el-tooltip placement="top">         
	<template slot="content">
     	<p style="max-width:500px;">提示内容</p>
  	</template>
   	<div class="info-mes">展示内容</div>
</el-tooltip>
```