public class RecursivePractice {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//fibonacci2(9);
		//sumOfDigits(199)
		//PowersOf2(3)
		//PowersOf22(5);
		//PowersOfNum(3, 3);
		//isPalindrome("bob");
		//numberOfDigits(390906)
		//isPalindromeRecursion("racecar");
		
		
		
		
		
	}
	public static int sumOfDigits(int num){
		if(num >0)
			return num%10+ sumOfDigits(num/10);
		else
			return num;

	}
	public static int PowersOf2( int exp){
		int product = 1;
		for(int i =1; i<=exp; i++){
			product *=2;
		}
		return product;
	}
	public static int PowersOf22(int exp){
		if( exp >1)
			return 2* PowersOf22( exp-1);
		else
			return 2;
	}
	public static int PowersOfNum(int base,int exp){
		 if(exp>1)
			 	return base * PowersOfNum(base, exp-1);
		 else
			 return base;
		
	}
	public static boolean isPalindrome(String str){
		int n = str.length();
		  for (int i = 0; i < (n/2); ++i) {
		     if (str.charAt(i) != str.charAt(n - i - 1)) {
		         return false;
		     }
		  }

		  return true;
		}
	public static int numberOfDigits(int num){
		if(num >0){
			return  1 + numberOfDigits(num/10);
	}
	else{
		return 0;
	}
	}
	
		
	public static boolean isPalindromeRecursion(String str) { 
		if (str == "") { return false; } 
		String reversed = reverse(str); 
		return str.equals(reversed); } 
	
	public static String reverse(String str) 
	{ if (str == null) { return null; } 
	if (str.length() <= 1) { return str; }
	return reverse(str.substring(1)) + str.charAt(0); 
	}

	

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
