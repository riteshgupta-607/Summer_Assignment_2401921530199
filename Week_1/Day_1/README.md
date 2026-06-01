// 1. Two sum problem
// brute force approach
import java.util.* ;
class Main {
    public static void twosum(int nums[] , int target){
        int arr[] = new int[2] ;
        for(int i = 0 ; i<nums.length ; i++){
            int start = nums[i] ;
        for(int j = i+1 ; j<nums.length ; j++){
            int next = nums[j] ;
            if(start + next ==target){
                arr[0] = i;
                arr[1] = j ;
            }
        }
        }
        System.out.println("result is..") ;
       System.out.print(arr[0]+","+arr[1]) ;
    }
    
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in) ;
        System.out.println("Enter the size of an array") ;
        int n = sc.nextInt() ;
        int nums[] =  new int[n] ;
        System.out.println("Enter the elements in an array") ;
        for(int i = 0 ; i<n ; i++){
            nums[i] = sc.nextInt() ;
        }
        System.out.println("Array elements are :");
        for(int i = 0 ; i<n ; i++){
            System.out.print(nums[i]+",") ;
        }
        System.out.println() ;
        System.out.println("Enter target sum") ;
        int target = sc.nextInt() ;
        twosum(nums,target);
        
        
    }
}

//2. remove duplicates from sorted array
import java.util.* ;
class Main {
    public static int removeduplicates(int nums[] ){
        if(nums.length<=1)
        System.out.println(nums.length) ;
        int indx = 1 ;
        for(int i = 1 ; i<nums.length; i++){
            if(nums[indx-1]!=nums[i]){
                nums[indx] = nums[i];
                indx++ ;
                
            }
        }
        return indx ;
    }
    
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in) ;
        System.out.println("Enter the size of an array") ;
        int n = sc.nextInt() ;
        int nums[] =  new int[n] ;
        System.out.println("Enter the elements in an array") ;
        for(int i = 0 ; i<n ; i++){
            nums[i] = sc.nextInt() ;
        }
        System.out.println("Array elements are :");
        for(int i = 0 ; i<n ; i++){
            System.out.print(nums[i]+",") ;
        }
        System.out.println() ;
      System.out.println(removeduplicates(nums)) ;
        
        
    }
}


// 3. best time to buy and sell stock
import java.util.* ;
class Main {
    public static int maxprofit(int prices[] ){
        int buyprice = Integer.MAX_VALUE ;
        int maxProfit = 0 ;
        for(int i = 0 ; i<prices.length ; i++){
            if(buyprice < prices[i]){
                int profit = prices[i] - buyprice ;
                 maxProfit = Math.max(maxProfit , profit) ;
            }
            else
            buyprice = prices[i] ;
        }
        return maxProfit ;
    }
    
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in) ;
        System.out.println("Enter the size of an array") ;
        int n = sc.nextInt() ;
        int prices[] =  new int[n] ;
        System.out.println("Enter the prices ") ;
        for(int i = 0 ; i<n ; i++){
            prices[i] = sc.nextInt() ;
        }
        System.out.println("Array elements are :");
        for(int i = 0 ; i<n ; i++){
            System.out.print(prices[i]+",") ;
        }
        System.out.println() ;
      System.out.println("the maximum profit  is"+" " + maxprofit(prices)) ;
        
        
    }
}
