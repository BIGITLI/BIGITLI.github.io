---
layout: post
title: 检测一个checkbox的选中状态
description: 前台页面问题
categories:
- pageQuestions 
tags:
- checkbox
---

##工作中遇到的问题以及解决方案##
###前台页面问题###
###检测一个checkbox的选中状态，直接用 .attr("checked")，无论是否选中，返回值都是 undefined 未定义   
如以下代码：  
	<
input  id="test" type="checkbox" 	checked="checked"/>  
alert(  $("#test").attr("checked")   );结果为undefined
解决方案：
  
1. 查看$("#test")的属性树结构得到解决方案，应该通过$("#test")[0].checked获取选中状态
