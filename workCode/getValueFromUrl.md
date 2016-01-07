##工作中积累的常用代码##
###前台js###
###获取当前页面路径中指定参数的值
如以下代码：  

	function getParameter(param)
	{
	  var query = window.location.search; //获取URL地址中？后的所有字符  
	  var iLen = param.length; //获取传入参数名称长度  
	  var iStart = query.indexOf(param); //获取传入参数名称的真实索引  
	  if (iStart == - 1) //-1为没有该参数  
	  return '';
	  iStart += iLen + 1;
	  var iEnd = query.indexOf('&', iStart); //获取第二个参数的真实索引  
	  if (iEnd == - 1) //只有一个参数  
	  return query.substring(iStart); //获取单个参数的参数值  
	  return query.substring(iStart, iEnd); //获取第二个参数的值  
	}