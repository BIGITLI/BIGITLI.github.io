##工作中遇到的问题以及解决方案##
###前台页面问题###
###在EL表达式中显示“yyyy-MM-dd”格式的日期  
解决方案：
  
1. 在页面上导入<%@ taglib prefix="fmt" uri="http://java.sun.com/jsp/jstl/fmt" %>  
2. 格式化日期<fmt:formatDate value="${XXX}" pattern="yyyy-MM-dd"/>  
3.  Value ：EL表达式取的日期值;Pattern：输出的日期格式；