---
title: element-ui tooltip手动设置宽度
type: article
tag: Element UI
abbrlink: 2736856151
date: 2021-07-29 00:00:00
---

```
<el-tooltip placement="top">         
	<template slot="content">
     	<p style="max-width:500px;">提示内容</p>
  	</template>
   	<div class="info-mes">展示内容</div>
</el-tooltip>
```