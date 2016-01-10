##工作中积累的常用代码##
###java后台###
###后台发送post请求将长链接转换为短链接
如以下代码：  
  
	Map<String, String> paramsMap = Maps.newHashMap();
	paramsMap.put("url",reserveUrl);
	//调用转换接口
	Document doc = Jsoup.connect("http://dwz.cn/create.php").data(paramsMap).post();
	String urlBack=doc.text();
	JSONObject jo=JSONObject.parseObject(urlBack);
	String shortUrl=jo.getString("tinyurl")