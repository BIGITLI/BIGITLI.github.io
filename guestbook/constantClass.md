##工作中积累的常用代码##
###java后台###
###常量类
如以下代码：  
  
	public class ReserveStatusManager {
  
		//预定   
		public final static int ORDER_REVERSE = 1;  

		//预定逾期  
		public final static int ORDER_REVERSE_OVERDUE=2;
  
		//点菜中  
		public final static int ORDER_REVERSE_DCZ=3;

		//提交状态  
		public final static int ORDER_REVERSE_TJ=4;

		//预定取消  
		public final static int ORDER_REVERSE_CANCEL=5;

		//处理完成
		public final static int ORDER_REVERSE_FINISH=6;
		//获取状态名称
		public static String getOrderStatusName(int status){  
			HashMap<Integer, String> map = new HashMap<Integer, String>();  
			map.put(ORDER_REVERSE, "预定");  
			map.put(ORDER_REVERSE_OVERDUE,"预定逾期");  
			map.put(ORDER_REVERSE_DCZ,"点菜中");   
			map.put(ORDER_REVERSE_TJ, "提交预订单");  
			map.put(ORDER_REVERSE_CANCEL, "预定取消");  
			map.put(ORDER_REVERSE_FINISH,"处理完成");  
			return map.get(status);  
		}  
	}