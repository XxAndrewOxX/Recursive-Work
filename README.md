# Recursive-Work
public class RecursivePractice {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//fibonacci2(9);
		System.out.println(sumOfDigits(0122));
		//PowersOf2(3);
		//PowersOf22(4);
		//PowersOfNum(14, 9);
		//isPalindrome("dragon");
		//numberOfDigits(36);
		//isPalinedromeRecursion("Box");
		
		
		
		
		
	}
	public static int sumOfDigits(int num){
		if(num >0)
			return num%10+ sumOfDigits(num/10);
		else
			return num;

	}
	public static int PowersOf2( int exp){
		int product = 1;
		for(int i =0; i<=product; i++){
			product *=2;
		}
		return product;
	}
	public static int PowersOf22(int exp){
		if( exp >0)
			return 2* PowersOf22( exp-1);
		else
			return exp;
	}
	public static int PowersOfNum(int base,int exp){
		 if(exp>0)
			 	return base * PowersOfNum(base, exp-1);
		 else
			 return base;
		
	}
	public static boolean isPalindrome(String str){
		int len = str.length();
		String	str1 = str.substring(0, len/2);
		String str2 = str.substring(len/2);
		if((str2+str1).equals(str)){
			return true;
		}
		else{
			return false;
		}
		}
	public static int numberOfDigits(int num){
		if(num >0){
			return  1 + numberOfDigits(num/10);
	}
	else{
		return 0;
	}
	}
	public static boolean isPalinedromeRecursion( String str){
		if( str.charAt(0) == str.charAt(str.length()-1)){
			return isPalinedromeRecursion(str.substring(1, str.length()-1));
		}
		else if (str.length() == 0 || str.length() == 1){
			return true;
		}
		else
			return false;
	}


	/*public static String fibonacci2(int term){
		if(term>2)
			return  fibonacci1(term-1) +""+ fibonacci1(term-2) ;
		else if(term<2 && term>0)
			return " ,"+fibonacci1(1) ;
		else{
			return " ,"+fibonacci1(2);	
				}
	}
	public static int fibonacci1(int num) { 
		if (num == 1) { return 1; } 
		if (num == 2) { return 1; } 
		return fibonacci1(num - 1) + fibonacci1(num - 2); }

	} */
	public static int fibonacci1(int term)  {
	    if(term == 0)
	        return 0;
	    else if(term == 1)
	      return 1;
	   else
	      return fibonacci1(term - 1) + fibonacci1(term - 2);
	}
	public static void fibonacci2(int num){
		for(int i =1; i<=num-1; i++){
			System.out.print(fibonacci1(i)+", ");
		}
		System.out.print(fibonacci1(num));
	}
}
