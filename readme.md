###字符串首字母转大写

	public static String captureName(String name)
	{
   		name = name.substring(0, 1).toUpperCase() + name.substring(1);
		return  name;
        char[] cs=name.toCharArray();
        cs[0]-=32;
        return String.valueOf(cs);
     }
    
1. 通过调用方法来实现，将首字母截取，转化成大写然后再串上后面的
		
		name = name.substring(0, 1).toUpperCase() + name.substring(1);
		return  name;		

2. 进行字母的ascii编码前移（这种更快）
		
		char[] cs=name.toCharArray();
        cs[0]-=32;
        return String.valueOf(cs);
        
3. New branch