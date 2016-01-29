---
layout: post
title: 关于cookie的相关操作
description: 前台js
categories:
-  WorkCode/page
tags:
- cookie
---

##工作中积累的常用代码##
###前台js###
###关于cookie的相关操作
如以下代码：  

	//添加cookie  
	//不设定过期时间，浏览器关闭时cookie自动消失  
	function addCookie(objName,objValue,objHours){
	    var str = objName + "=" + escape(objValue);
	    if(objHours > 0){
	        var date = new Date();
	        var ms = objHours*3600*1000;
	        date.setTime(date.getTime() + ms);
	        str += "; expires=" + date.toGMTString()+";path=/";
	   }
	   document.cookie = str;
	}
 
	//两个参数，一个是cookie的名字，一个是值
	//此 cookie 将被保存 30 天
	function setCookie30Days(name,value)
	{
	  var Days = 30; //此 cookie 将被保存 30 天
	  var exp = new Date();    //new Date("December 31, 9998");
	  exp.setTime(exp.getTime() + Days*24*60*60*1000);
	  document.cookie = name + "="+ escape (value) + ";expires=" + exp.toGMTString()+";path=/";
	}
	
	//获取指定名字cookie的值
	function getCookie(name)
	{
	    var arr,reg=new RegExp("(^| )"+name+"=([^;]*)(;|$)");
	    if(arr=document.cookie.match(reg))
			return unescape(arr[2]);
	    else
	    	return null;
	}

	//删除cookie
	function delCookie(name)
	{
	  var exp = new Date();
	  exp.setTime(-1);
	  var cval=getCookie(name);
	  if(cval!= undefined) 
	  	document.cookie= name + "=''"+";expires="+exp.toGMTString()+";path=/";
	
	  return cval;
	}
	
	//删除指定路径下的cookie
	function delCookie(name,path)
	{
	  var exp = new Date();
	  exp.setTime(-1);
	  var cval=getCookie(name);
	  if(cval!= undefined) 
	    document.cookie= name + "=''"+";expires="+exp.toGMTString()+"; path=" + path;
	
	  return cval;
	}
	
	//获取主机地址
	function getHostPath(){
		var curWwwPath=window.document.location.href;
		var pathName=window.document.location.pathname;
		var pos=curWwwPath.indexOf(pathName);
		return curWwwPath.substring(0,pos);
	}
	
	//获取当前项目地址
	function getRootPath(){
		var curWwwPath=window.document.location.href;
		var pathName=window.document.location.pathname;
		var pos=curWwwPath.indexOf(pathName);
		var localhostPaht=curWwwPath.substring(0,pos);
		var projectName=pathName.substring(0,pathName.substr(1).indexOf('/')+1);
		return (localhostPaht+projectName);
	}
