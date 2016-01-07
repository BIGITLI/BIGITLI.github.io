##工作中积累的常用代码##
###前台js###
###利用数组和对象封装数据并转换为json字符串###
如以下代码：
  
	var ruleArray=[]; //定义数组   
	$(".form-group").each(function(){  
	var consumption=$(this).find(".consumption").val();  
	var voucherId=$(this).find(".voucherId").val();  
	var rule={};//定义对象  
	rule["consumption"]=consumption;  
	rule["voucherId"]=voucherId;
	rule["specialOfferId"]=specialOfferId;  
	ruleArray.push(rule);  
	});  
	var ruleListStrUpDate=JSON.stringify(ruleArray);  

用于发送ajax时带的数据