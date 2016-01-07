##工作中积累的常用代码##
###前台js###
###倒计时
如以下代码：  

	var count = 90;  
	var myCountDown;  
	//按钮计时函数  
	function countDown() {
	  count--;  
	  $('#sen_vc').html('请稍等 ' + count + ' 秒！');  
	  if (count == 0) {  
	    $('#sen_vc').attr('disabled',false);  
	    $('#sen_vc').css('background-color','#fc6a14');  
	    $("sen_vc").css("border-color",'#fc6a14');  
	    $('#sen_vc').html('发送验证码');   
	 	//结束倒计时（传入setIntervaL的ID结束调用setInterval函数）  
	    clearInterval(myCountDown);  
	    count = 90;  
	  }  
	}  
	
	//按钮点击事件时调用一下语句
	//调用倒计时函数   
	//每次调用，返回唯一标志setInterval的ID  
	myCountDown = setInterval(countDown, 1000);
