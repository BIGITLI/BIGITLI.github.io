##工作中积累的常用代码##
###java后台###
###枚举类
如以下代码：  
 
	public enum PayMethod {
		HONGCHONG("hongchong","红冲"),
		CASHPAY("cashPay","现金支付"),
		BACKPAY("bankPay","银行卡支付"),
		ZHIFUBAOPAY("zhifubaoPay","支付宝支付"),
		WEIXINPAY("weixinPay","微信支付"),
		FREEPAY("freePay","免单"),
		COUPONPAY("couponPay", "优惠券支付"),
		DISCOUNTPAY("dicountPay","折扣金额"),
		ZHAOLING("zhaoling","找零");
		
		private String index;
		private String name;
		private PayMethod(String index,String name){
			this.index = index;
			this.name = name;
		}
		
		/**
		 * 获取支付方式名称
		 * @param index
		 *    支付方式标识
		 * @return
		 */
		public static String getPayName(String index){
			PayMethod pm = null;
			for ( PayMethod pay : PayMethod.values()) {
				if(pay.getIndex().equals(index)){
					pm = pay;
				}
			}
			if(pm == null){
				return "未知支付方式";
			}
			return pm.getName();
		}
	
		/**
		 * 获取支付方式名称
		 * @param paymethod
		 * @return
		 */
		public static String getPayName(PayMethod paymethod){
			
			return paymethod.getName();
		}
		
		
		/**
		 * @return the index
		 */
		public String getIndex() {
			return index;
		}
	
	
		/**
		 * @return the name
		 */
		public String getName() {
			return name;
		}
	
	
		/**
		 * @param index the index to set
		 */
		public void setIndex(String index) {
			this.index = index;
		}
	
	
		/**
		 * @param name the name to set
		 */
		public void setName(String name) {
			this.name = name;
		}

	}   
