##工作中积累的常用代码##
###java后台###
###MD5加密
如以下代码：  
  
	public class MD5 {

		/**
		 * 对string进行MD5加密(标准方法)
		 * 
		 * @param string
		 *            String
		 * @return String
		 */
		public static String generateMD5String(String string) {
			String result = "";
			try {
				MessageDigest m = MessageDigest.getInstance("MD5");
				m.update(string.getBytes("UTF8"));
				byte s[] = m.digest();
				for (int i = 0; i < s.length; i++) {
					result += Integer.toHexString((0x000000ff & s[i]) | 0xffffff00)
							.substring(6);
				}
			} catch (Exception e) {
				result = null;
			}
	
			return result;
		}
	
		/**
		 * 对string进行md5加密后与md5String进行比较
		 * 
		 * @param string
		 *            String 要进行md5加密的字符串
		 * @param md5String
		 *            String 预期得到加密后的md5密文
		 * @return boolean
		 */
		public static boolean compareMD5String(String string, String md5String) {
			boolean result;
			if (generateMD5String(string).equalsIgnoreCase(md5String)) {
				result = true;
			} else if (generateMD5StringOld(string).equalsIgnoreCase(md5String)) {
				result = true;
			} else {
				result = false;
			}
			return result;
		}
	
		/**
		 * 兼容以前的md5加密方法
		 * 
		 * @param string
		 *            String
		 * @return String
		 */
		public static String generateMD5StringOld(String string) {
			try {
				byte[] res = string.getBytes();
				MessageDigest md = MessageDigest.getInstance("MD5");
				byte[] result = md.digest(res);
				for (int i = 0; i < result.length; i++) {
					md.update(result[i]);
				}
				byte[] hash = md.digest();
				StringBuffer d = new StringBuffer("");
	
				for (int i = 0; i < hash.length; i++) {
					int v = hash[i] & 0xFF;
					if (v < 16) {
						d.append("0");
					}
					d.append(Integer.toString(v, 16).toUpperCase() + "");
				}
				return d.toString();
			} catch (Exception e) {
				return null;
			}
		}
	}