# S_NIKHIL
This is my first Git Repository.
It is my learnings, not any project. I am writing code here only for easy access in any device which is helpful for me.
I will upload my projects and give description here in future.

// Q.1 -> PRIME NUMBER FORM 1 TO N.

import java.util.*;
public class JavaBasics{

    public static boolean isPrime(int n){
        if(n==2){
            return true;
        }
        for(int i=2;i<=Math.sqrt(n);i++){
            if(n%i==0){
                return false;  
            }
        }  
            return true;
    }
    public static void rangePrime(int n){
        
        if(isPrime(n)){
            System.out.println("Prime no are:"+n);
        }else{
            System.out.println("Prime not are:"+n);
        }
    }
    public static void  main(String args[]){
        Scanner sc=new Scanner (System.in);
        int n=sc.nextInt();
        rangePrime(n);

    }
}

// Q.2 -> BINARY TO DECIMAL.

import java.util.*;
public class JavaBasics{

    public static void binToDec(int binNum){
        int urNum=binNum;
        int pow=0;
        int dec=0;
        while(binNum>0){
            int lastDigit=binNum%10;
            dec=dec+lastDigit*(int)Math.pow(2,pow);
            pow++;
            binNum=binNum/10;
        }
        System.out.println("The Decimal of Binary number "+urNum+" is:" +dec);
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter ur Binary number:");
        int n=sc.nextInt();
        binToDec(n);
    }
}


// Q.3 -> DECIMAL TO BINARY.

import java.util.*;
public class JavaBasics{

    public static void DecToBin(int DecNum){
        int urNum=DecNum;
        int binNum=0;
        int rmndr=0;
        int pow=0;
        while(DecNum>0){
            rmndr=DecNum%2;
            binNum=binNum+rmndr*(int)Math.pow(10,pow);
            pow++;
            DecNum=DecNum/2;
        }
        System.out.println("ur Binary number of "+urNum+" is:"+binNum);
    }

    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter ur Number:");
        int n=sc.nextInt();
        DecToBin(n);
    }
}

// Q.4 -> SUM OF DIGITS OF THAT NUMBER.

import java.util.*;
public class JavaBasics{

    public static int digSum(int n){
        int DigSum=0;  
        while(n>0){
            int ld=n%10;
            DigSum=DigSum+ld;
            n=n/10;
          }return DigSum;
          
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter ur number:");
        int n=sc.nextInt();
        System.out.println("The sum of digits is:"+digSum(n));
    }
}

// Q.5 -> CHECK IF A NUBER IS PALINDROME.

import java.util.*;
public class JavaBasics{

    public static long revNum(long n){
         long num=0;
        while(n>0){
            long ld=n%10;
            num=num*10+ld;
            n=n/10;
        }return num;
    }
    public static void palindrome(long n){
        if(n==revNum(n)){
            System.out.println("ur number is palindrome:"+n);
        }else{
            System.out.println("ur number is not palindrome:"+n);
        }
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter ur number :");
        long n=sc.nextLong();
        palindrome(n);
    }
}

// Q.6 -> RECTANGLE (HOLLOW) SHAPE WITH STAR.

import java.util.*;
public class JavaBasics{

    public static void hollowRectangle(int totRows,int totColmns){
        for(int row=1;row<=totRows;row++){
            for(int colmn=1;colmn<=totColmns;colmn++){
                if(row==1||row==totRows||colmn==1||colmn==totColmns){
                System.out.print("* ");
            }else{
                System.out.print("  ");
            }
            }System.out.println();
        }
    }
    public static void main(String args[]){
        hollowRectangle(4,5);
    }
}

// Q.7 -> HALF PYRAMID WITH STAR.

import java.util.*;
public class JavaBasics{

    public static void half_pyramid(int totRows){
        for(int row=1;row<=totRows;row++){
            for(int j=1;j<=row;j++){
                System.out.print("*");
            }System.out.print("\n");
        }
    }
    public static void main(String args[]){
        half_pyramid(4);
    }
}

// Q.8 -> INVERTED & ROTATED HALF PYRAMID WITH STAR.

import java.util.*;
public class JavaBasics{

    public static void invrtd_rotated_half_pyramid(int totRows){
        for(int row=1;row<=totRows;row++){
            for(int i=1;i<=totRows-row;i++){
                System.out.print(" ");
            }
            for(int j=1;j<=row;j++){
                System.out.print("*");
            }System.out.print("\n");
        }
    }
    public static void main(String args[]){
        invrtd_rotated_half_pyramid(4);
    }
}

// Q.9 -> INVERTED HALF PYRAMID WITH NUMNBERS.

import java.util.*;
public class JavaBasics{

    public static void inverted_half_numPyramid(int totLine){
        for(int line=1;line<=totLine;line++){
            for(int i=1;i<=totLine-line+1;i++){
                System.out.print(i);
            }System.out.print("\n");
        }
    }
    public static void main(String args[]){
        inverted_half_numPyramid(5);
    }
}

// Q.10 -> FLOYD'S TRIANGLE.

import java.util.*;
public class JavaBasics{

    public static void triangle_folyd(int totLine){
        int counter=1;
        for(int line=1;line<=totLine;line++){
            for(int i=1;i<=line;i++){
                System.out.print(counter+" ");
                counter++;
            }System.out.print("\n");
        }
    }
    public static void main(String args[]){
        triangle_folyd(5);
    }
}

// Q.11 -> 0-1 TRIANGLE.

import java.util.*;
public class JavaBasics{

    public static void zero_one_triangle(int totRows){
        for(int row=1;row<=totRows;row++){
            for(int colmn=1;colmn<=row;colmn++){
                if((row+colmn)%2==0){
                    System.out.print(1);
                }else{
                    System.out.print(0);
                }
            }System.out.println();
        }
    }
    public static void main(String args[]){
           zero_one_triangle(5); 
    }
}

// Q.12 -> BUTTERFLY PATTERN.

import java.util.*;
public class JavaBasics{

    public static void butterfly_pattern(int totLine){
        for(int line=1;line<=totLine;line++){
            for(int i=1;i<=line;i++){
                System.out.print("*");
            }for(int j=1;j<=2*(totLine-line);j++){
                System.out.print(" ");
            }for(int i=1;i<=line;i++){
                System.out.print("*");
            }
            System.out.print("\n");
    }for(int line=totLine;line>=1;line--){
            for(int i=line;i>=1;i--){
                System.out.print("*");
            }for(int j=2*(totLine-line);j>=1;j--){
                System.out.print(" ");
            }for(int i=line;i>=1;i--){
                System.out.print("*");
            }
            System.out.print("\n");
           }
    }
    public static void main(String args[]){
            butterfly_pattern(10);
    }
}

// Q.13 -> SOLID RHOMBUS PATTERN.

import java.util.*;
public class JavaBasics{

    public static void solid_rhombus_pattern(int totLine){
        for(int line=1;line<=totLine;line++){
            //space
            for(int i=1;i<=totLine-line;i++){
                System.out.print(" ");
            }for(int j=1;j<=totLine;j++){
                System.out.print("*");
            }
            System.out.print("\n");
        }
    }
    public static void main(String args[]){
            solid_rhombus_pattern(5);
    }
}

// Q.14 -> HOLLOW RHOMBUS PATTERN.

import java.util.*;
public class JavaBasics{

    public static void hollow_rhombus(int totLine){
        for(int line=1;line<=totLine;line++){
            //space
            for(int i=1;i<=totLine-line;i++){
                System.out.print("  ");
        }for(int colmn=1;colmn<=totLine;colmn++){
            if(line==1||line==totLine||colmn==1||colmn==totLine){
                System.out.print("* ");    
            }else{
                System.out.print("  ");
                }
            }System.out.print("\n");
        }
    }
    public static void main(String args[]){
        hollow_rhombus(5);
    }
}

------------OR------------

import java.util.*;
public class JavaBasics{

    public static void hollow_rhombus(int totLine){
        for(int line=1;line<=totLine;line++){
            //space
            for(int i=1;i<=totLine-line;i++){
                System.out.print("  ");
            }//for 1st & last line star
            if(line==1||line==totLine){
                for(int j=1;j<=totLine;j++){
                System.out.print("* ");    
                }
                //next line
                System.out.print("\n");
            }else{
                //star
                System.out.print("* ");
                //space
                for(int k=1;k<=totLine-2;k++){
                    System.out.print("  ");
                }
                //star
                System.out.print("* ");
                //next line
                System.out.print("\n");
            }
        }
    }
    public static void main(String args[]){
        hollow_rhombus(5);
    }
}

// Q.15 -> DIAMOND PATTERN.

import java.util.*;
public class JavaBasics{

    public static void diamond_pattern(int totLine){
        for(int line=1;line<=totLine;line++){
            for(int i=1;i<=totLine-line;i++){
                System.out.print(" ");
            }for(int j=1;j<=line*2-1;j++){
                System.out.print("*");
            }
           System.out.print("\n");
        }for(int line=totLine;line>=1;line--){
            for(int i=totLine-line;i>=1;i--){
                System.out.print(" ");
            }for(int j=line*2-1;j>=1;j--){
                System.out.print("*");
            }
            System.out.print("\n");
        }
    }
    public static void main(String args[]){
        diamond_pattern(4);
    }
}

// Q.16 -> LINEAR SEARCH IN ARRAY.

import java.util.*;
public class JavaBasics{

    public static int linearSearch(int numbers[], int key){
        for(int i=0;i<=numbers[i];i++){
            if(numbers[i]==key){
                return i;
            }
        }return -1;
    }
    public static void main(String args[]){
     Scanner sc = new Scanner(System.in);

        // 1. Array ka size pucha
        System.out.print("Array ka size enter karein: ");
        int n = sc.nextInt();

        // 2. Array create kiya
        int[] numbers = new int[n];

        // 3. Loop se values input li
        System.out.println("Ab " + n + " elements enter karein:");
        for (int i = 0; i < n; i++) {
            System.out.print("Element " + (i + 1) + ": ");
            numbers[i] = sc.nextInt();
        }

        // 4. Output dikhane ke liye
        System.out.println("\nAapka Array yeh hai:");
        for (int i = 0; i < n; i++) {
            System.out.print(numbers[i] + " ");
        }System.out.println("\n");
        int key=5;
        int index=linearSearch(numbers,  key);
        if(index==-1){
            System.out.println("NOT found");
        }else{
            System.out.println("key is at index:"+index);
        }
    } 
}


// Q.17 -> LARGEST/SMALLEST NUMBER IN ARRAY.

import java.util.*;
import java.util.Scanner;
public class JavaBasics{

    public static int getLargest(int numbers[]){
        int largest=Integer.MIN_VALUE;//- infinity
        int smallest=Integer.MAX_VALUE;//+ infinity0
        for(int i=0;i<numbers.length;i++){
            if(largest<numbers[i]){
                largest=numbers[i];
            }    
        }
        for(int i=0;i<numbers.length;i++){
            if(smallest>numbers[i]){
                smallest=numbers[i];
            }
        }System.out.println("smallest value is:"+smallest);
        return largest;
        
    }    
    public static void main(String args[]){
       Scanner sc=new Scanner(System.in);
       //size of array
       System.out.print("Enter size of num array: ");
       int n=sc.nextInt();
       int numbers[]=new int[n];
       System.out.println("Enter ur num array-");
       for(int i=0;i<n;i++){
       System.out.print("Element "+(i+1)+": "); 
        numbers[i]=sc.nextInt();
       }
       System.out.println("largest value is:"+getLargest(numbers));
    }
}

// Q.18 -> BINARY SEARCH IN A SORTED ARRAY.

import java.util.*;
public class JavaBasics{

    public static int binarySearch(int numbers[],int key){
        int start=0,end=numbers.length-1;
        while(start<=end){
            int mid=(start+end)/2;
            if(numbers[mid]==key){
                return mid;
            }
            if(numbers[mid]>key){
                end=mid-1;
            }else{
                start=mid+1;
            }
        }return -1;
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10,12,14};
        int key=15;
        int index=binarySearch(numbers,key);
        System.out.println("index of your key is:"+index);
    }
}

// Q.19 -> REVERSE OF AN ARRAY.

import java.util.*;
public class JavaBasics{

    public static void reverseArray(int numbers[]){
        int first=0,last=numbers.length-1;
        while(first<last){
            int temp=numbers[first];
            numbers[first]=numbers[last];
            numbers[last]=temp;
            first++;
            last--;
        }
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10};
        reverseArray(numbers);
        for(int i=0;i<numbers.length;i++){
            System.out.print(numbers[i]+" ");
        }
    }
}

// Q.20 -> PRINT PAIR FROM AN ARRAY.

import java.util.*;
public class JavaBasics{

    public static void printPair(int numbers[]){
        for(int i=0; i<numbers.length; i++){
            int curnt=numbers[i];
            for(int j=i+1; j<numbers.length; j++){
                System.out.print("("+curnt+","+numbers[j]+")");
            }
            System.out.println();
        }
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10};
        printPair(numbers);
    }
}

// Q.21 -> PRINT AND COUNT SUBARRAY OF A GIVEN ARRAY.

import java.util.*;
public class JavaBasics{

    public static void printSubArray(int numbers[]){
        int ttlsbary=0;
        for(int i=0; i<numbers.length;i++){
            int start=i;
            for(int j=i; j<numbers.length;j++){
                int end=j;
                for(int k=start; k<=end; k++){
                    System.out.print(numbers[k]+" ");
                }System.out.println();
                ttlsbary++;
            }System.out.println();
        }System.out.println("total subarray:"+ttlsbary);
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10};
        printSubArray(numbers);
    }
}

// Q.22 -> PRINT AND COUNT SUBARRAY OF A GIVEN ARRAY AND COMPUTE THE SUM OF THE ELEMENT OF EACH SUBARRAY ALSO FIND MINIMUM AND MAXIMUM SUM OF SUBARRAY.

import java.util.*;
public class JavaBasics{

    public static void printSubArray(int numbers[]){
        int ttlsbary=0;
        int sbarysum=0;
        int maxsum=0;
        for(int i=0; i<numbers.length;i++){
            int start=i;
            for(int j=i; j<numbers.length;j++){
                int end=j;
                for(int k=start; k<=end; k++){
                    System.out.print(numbers[k]+" ");
                    sbarysum=sbarysum+numbers[k]; 
                }System.out.println();
                System.out.println("sum of element:"+sbarysum);
                maxsum=sbarysum;
                sbarysum=0;
                ttlsbary++;
            }System.out.println("minimum sum of subArray is:"+numbers[start]+" \nmaximum sum of subArray is:"+maxsum+"\n");
        }System.out.println("total subarray:"+ttlsbary);
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10};
        printSubArray(numbers);
    }
}

// Q.23 -> FIND MAXIMUM SUM OF SUBARRAY (BRUTE FORCE).

import java.util.*;
public class JavaBasics{

    public static void maxSubArraySum(int numbers[]){
        int sbarysum=0;
        int maxsum=Integer.MIN_VALUE;
        for(int i=0; i<numbers.length;i++){
            int start=i;
            for(int j=i; j<numbers.length;j++){
                int end=j;
                for(int k=start; k<=end; k++){
                    sbarysum=sbarysum+numbers[k]; 
                }System.out.println("sum of element:"+sbarysum);
                if(maxsum<sbarysum){
                maxsum=sbarysum;
                }sbarysum=0;
            }
        }System.out.println("maximum sum of subArray is:"+maxsum+"\n");
    }
    public static void main(String args[]){
        int numbers[]={2,4,6,8,10};
        maxSubArraySum(numbers);
    }
}

// Q.24 -> FIND MAXIMUM SUBARRAY SUM (PREFIX SUM).

import java.util.*;
public class JavaBasics {

    public static void maxSubArraySum(int numbers[]){
        int sbArySum=0;
        int maxSum=Integer.MIN_VALUE;
        int prefix[]=new int [numbers.length];
        prefix[0]=numbers[0];
        for(int i=1; i<prefix.length; i++){
            prefix[i]=prefix[i-1] + numbers[i];
        }
        for(int i=0; i<numbers.length; i++){
            int start=i;
            for(int j=i; j<numbers.length; j++){
                int end=j;
                sbArySum= start==0 ? prefix[end] : prefix[end] - prefix[start-1];
                if(maxSum<sbArySum){
                    maxSum=sbArySum;
                }
            }
        }System.out.println("maximum sum is:"+maxSum);
    }
    public static void main(String args[]){
        int numbers[]={1,-2,6,-1,3};
        maxSubArraySum(numbers);
    }
}

// Q.25 -> FIND MAXIMUM SUM OF SUBARRAY (KADAN'S ALGORITHM)  --> (ALL ARRAY ELEMENT ARE 'NOT' NEGATIVE 'OR' MIX OF (-VE) AND (+VE) ELEMENT).         " [  VERY IMPORTANT QUESTION  ] "

import java.util.*;
public class JavaBasics{

    public static void kadanes(int numbers[]){
        int sbArySum=0;
        int maxSum=Integer.MIN_VALUE;
        for(int i=0; i<numbers.length; i++){
            sbArySum = sbArySum + numbers[i];
            if(sbArySum<0){
                sbArySum=0;
            } 
            maxSum=Math.max(maxSum,sbArySum);
        }System.out.println("max sum is:"+maxSum);
    }
    public static void main(String args[]){
        int numbers[]={-2,-3,4,-1,-2,1,5,-3};
        kadanes(numbers);
    }
}

// Q.26 -> FIND MAXIMUM SUM OF SUBARRAY (KADAN'S ALGORITHM)  --> ( ALL ARRAY ELEMENT ARE NEGATIVE 'OR' MIX OF (-VE) AND (+VE) ELEMENT ).         " [  VERY IMPORTANT QUESTION  ] "

import java.util.*;
public class JavaBasics{

    public static void kadanes(int numbers[]){
        int sbArySum=0;
        int mxsbArySumNeg=0;
        int maxSum=Integer.MIN_VALUE;
        int mxSumNeg=Integer.MIN_VALUE;
        for(int i=0; i<numbers.length; i++){
            sbArySum = sbArySum + numbers[i];
            if(sbArySum<0){
                mxsbArySumNeg=sbArySum;
                sbArySum=0;
            } 
            maxSum=Math.max(maxSum,sbArySum);
            mxSumNeg=Math.max(mxSumNeg,mxsbArySumNeg);
        }if(mxsbArySumNeg<0 && maxSum==0){
            System.out.println("max sum is:"+mxSumNeg);
        }else{
            System.out.println("max sum is:"+maxSum);
        }
    }
    public static void main(String args[]){
        int numbers[]={-2,-4,-6,-8,-10};
        kadanes(numbers);
    }
}

// Q.27 -> CALCULATION TRAPED RAIN WATER OF GIVEN BAR.                                  " [  VERY IMPORTANT QUESTION  ] "

import java.util.*;
public class JavaBasics{

    public static int trapedRainwater(int height[]){
        int n=height.length;
        int width=1;
        int trapedWater =0;

        //left max boundry - array
        int leftMax[]=new int[n];//height of leftMax array is equals to n(height array ke length ke barabar)
        leftMax[0]=height[0];
        for(int i=1; i<n; i++){
            leftMax[i]=Math.max(height[i],leftMax[i-1]);
        }
        //right max boundry - array
        int rightMax[]=new int[n];
        rightMax[n-1]=height[n-1];
        for(int i=n-2; i>=0; i--){
            rightMax[i]=Math.max(height[i],rightMax[i+1]);
        }
        //calculation of water level and traped water
        for(int i=0; i<n-1; i++){
            int wtrLvl=Math.min(leftMax[i],rightMax[i]);
            trapedWater = trapedWater + (wtrLvl-height[i])*width;
        }
        return trapedWater;
    }
    public static void main(String args[]){
        int height[]={4,2,0,6,3,2,5};
        System.out.println("traped Rainwater is : "+trapedRainwater(height));
    }
}

// Q.28 -> CALCULATE MAX PROFIT IN STOCK ( BUY & SELL STOCKS ).

import java.util.*;
public class JavaBasics{

    public static int buyAndSellStocks(int prices[]){
        int buyPrice=Integer.MAX_VALUE;
        int maxProfit=0;
        for(int i=0; i<prices.length; i++){
            if( buyPrice < prices[i]){
                int profit= prices[i] - buyPrice; //profit of that day
                maxProfit=Math.max(maxProfit,profit);
            }else{
                buyPrice=prices[i]; //ussi din kharid liya
            }
        }return maxProfit;
    }
    public static void main(String args[]){
        int prices[]={7,1,5,3,6,4};
        System.out.println(" max profit is:"+buyAndSellStocks(prices));
    }
}
                                                      " ARRAY'S ASSIGNMENT "
//Question 1:Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.
Example 1:Input:nums = [1, 2, 3, 1]
Output: true 
Example 2:Input:nums = [1, 2, 3, 4]
Output: false 
Example 3:Input:nums = [1, 1, 1, 3, 3, 4, 3, 2, 4, 2]
Output: true 
Constraints:
•1 <= nums .  lengtth <= 105
•-109 <= nums [ i ] <= 109

import java.util.*;
public class JavaBasics{
    
    //main code means solution or logic.
    public static boolean checkRepetition(int nums[]){
        for(int i=0; i<nums.length-1; i++){
            for(int j=i+1; j<nums.length; j++){
                if(nums[i]==nums[j]){
                    return true;
                }
            }
        }return false;
    }

    
    public static void main(String args[]){
        //if you want to take array as input from user. otherwise u can simply write the array. 
        Scanner sc= new Scanner (System.in);
        System.out.print("Enter the size of array:");
        int n=sc.nextInt();
        //Array create kiya
        int nums[]=new int[n];
        System.out.println("Now Enter "+n+" elements:");
        for(int i=0; i<n; i++){
            System.out.print("Element "+(i+1)+":");
            nums[i]=sc.nextInt();
        }
        //output dikhane ke liye
        System.out.print("ur array:");
        for(int i=0; i<n; i++){
            System.out.print(nums[i]+" ");
        }  
        System.out.println("\n"+checkRepetition(nums));  
    }
}

//Question 2:There is an integer array nums sorted in ascending order (with distinct values).Prior to being passed to your function, nums is possibly rotated at an unknown pivot  index k (1  <=  k  <  nums.length)  such  that  the  resulting  array  is [nums[k], nums[k+1],   ...,   nums[n-1], nums[0],   nums[1],   ...,   nums[k-1]] (0-indexed).   For   example, [0,1,2,4,5,6,7] might be rotated at pivot index 3 and become [4,5,6,7,0,1,2].
Given the array nums after the possible rotation and an integer target, returnthe index oftarget if it is in nums, or -1   if it is not in nums.You must write an algorithm with O(log n) runtime complexity.
Example 1:Input:nums = [4,  5, 6, 7, 0, 1, 2], target = 0 
Output:   4 
Example 2:Input:nums = [4,  5, 6, 7, 0, 1, 2], target = 3
Output:   -1 
Example 3:Input:nums = [1], target = 0
Output:   -1 
Constraints:
•1 <= nums . lengtth <= 5000 
•-104 <= nums [ i ] <= 104
•All values of nums are unique.
•nums is an ascending array that is possibly rotated.
•-104 <= target <= 10

import java.util.*;
public class JavaBasics{

    public int minSearch(int[] nums){ 
        int left = 0; 
        int right = nums.length-1; 
        while(left < right){
            int mid = left + (right - left)/2; 
            if(mid >  0  &&   nums[mid-1]    >  nums[mid]){
                 return mid; 
                } else if(nums[left] <= nums[mid] && nums[mid] > nums[right]){ 
                    left = mid+1;
                } else{ 
                    right = mid-1; 
                } 
            } return left;
    }public int search(int[] nums, int target) {
        //min will have index of minimum element of nums 
        int min = minSearch(nums); 
        //find in sorted left 
        if(nums[min] <= target && target <= nums[nums.length-1]){ 
            return search(nums,min,nums.length-1,target); 
        } 
        //find in sorted right 
        else{ return search(nums,0,min,target); 

        } 
    }//binary search to find target in left to right boundary 
    public int search(int[] nums,int left,int right,int target){
        int l = left; 
        int    r  = right;
        //System.out.println(left+" "+right); 
        while(l <= r){ int mid = l + (r - l)/2; 
            if(nums[mid] ==   target){ 
                return mid; 
            } else if(nums[mid] > target){ 
                r = mid-1; 
            } else{ 
                l = mid+1; 
            } 
        } return -1; 
    }

    
    public static void main(String args[]){
        int nums[]={4,5,6,7,0,1,2};
        int target=2;
        JavaBasics obj=new JavaBasics();
        System.out.println(obj.search(nums,target));
    }
}

---------------------- MY SOLUTION (BRUTE FORCE) MAY BE WRONG IT IS IN LEARNING PHASE ----------------------

import java.util.*;
public class JavaBasics{

    public static int findTarget(int nums[]){
        int target=0;
        int rtrn=0;
        int bigNum=Integer.MAX_VALUE;
        for(int i=0; i<nums.length; i++){
            if(nums[i]<bigNum){
                bigNum=nums[i];
                if(target<bigNum){
                    rtrn = -1;
                }else{
                    int start=i;
                    int end=nums.length;
                    for(int j=start; j<end; j++){
                        if(target==nums[j]){
                            rtrn = j;
                        }
                    }
                }
            }   
        }return rtrn;
    }
    public static void main(String args[]){
        int nums[]={4,5,6,7,0,1,2};
        System.out.println(findTarget(nums));
    }
}

//Question 3:You  are  given  an  array prices where prices[i] is  the  price  of  a  given  stock  on  the ith day.
Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0. 
Example 1:Input:prices = [7, 1, 5, 3, 6,  4]   
Output:   5 
Explanation:Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5. 
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
Example 2:Input:Prices = [7, 6, 4,  3, 1]   
Output:   0 
Explanation:In this case, no transactions are done and the max profit = 0.
Constraints:
•1 <= prices . length <= 105
•0   <= prices [ i ] <= 104 

import java.util.*;
public class JavaBasics{

    public static int maxStockProfit(int prices[]){
        int buyPrice=Integer.MAX_VALUE;
        int maxProfit= 0;
        for(int i=0; i<prices.length; i++){
            if( buyPrice < prices[i]){
                int profit=prices[i] - buyPrice;
                maxProfit=Math.max(maxProfit,profit);
            }else{
                buyPrice=prices[i];
            }
        }return maxProfit;
    }
    public static void main(String args[]){
        int prices[]={8,7,5,3,2,1};
        System.out.println(maxStockProfit(prices));
    }
}

//Question 4:Given n non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
Example 1:
Input:height = [0, 1, 0,  2, 1, 0, 1, 3, 2, 1, 2, 1]
Output:   6
Explanation:The above elevation map (black section) is represented by array [0,1,0,2,1,0,1,3,2,1,2,1]. In this case, 6 units of rain water (blue section) are being trapped.
Example 2:
Input:height = [4, 2, 0, 3, 2, 5]
Output:   9 
Constraints:
•n == height . length
•1 <= n <= 2 * 104
•0 <= height [ i ] < = 105

import java.util.*;
public class JavaBasics{

    public static int trapedRainwater(int height[]){
        int n=height.length;
        int width=1;
        int trapedWater =0;

        //left max boundry - array
        int leftMax[]=new int[n];//height of leftMax array is equals to n(height array ke length ke barabar)
        leftMax[0]=height[0];
        for(int i=1; i<n; i++){
            leftMax[i]=Math.max(height[i],leftMax[i-1]);
        }
        //right max boundry - array
        int rightMax[]=new int[n];
        rightMax[n-1]=height[n-1];
        for(int i=n-2; i>=0; i--){
            rightMax[i]=Math.max(height[i],rightMax[i+1]);
        }
        //calculation of water level and traped water
        for(int i=0; i<n-1; i++){
            int wtrLvl=Math.min(leftMax[i],rightMax[i]);
            trapedWater = trapedWater + (wtrLvl-height[i])*width;
        }
        return trapedWater;
    }
    public static void main(String args[]){
        int height[]={4,2,0,6,3,2,5};
        System.out.println("traped Rainwater is : "+trapedRainwater(height));
    }
}

// Question 5: Given an integer array nums, return all the triplets [nums[i], nums[j], nums[k]] such that i != j, i != k, and j != k, and nums[i] + nums[j] + nums[k] == 0.
Notice that the solution set must not contain duplicate triplets.

Example 1:
Input:nums = [-1, 0,  1, 2, -1, -4]   
Output:   [ [-1, -1, 2] , [-1, 0, 1] ]
Example 2:
Input:nums = [ ]  
Output:   [ ]  
Example 3:
Input:nums = [ 0   ]  
Output:   [ ]  
Constraints:
• 0 <= nums . length <= 3000 
•-105 <= nums [ i ] <= 105

-----------BRUTE FORCE----------
import java.util.*;
public class JavaBasics{

    public static void returnTriplets(int nums[]){
        //String rtrn='0';
         System.out.print("[");
        for(int i=0; i<nums.length; i++){
            for(int j=i+1; j<nums.length; j++){
                for(int k=j+1; k<nums.length; k++){
                    if(nums[i]+nums[j]+nums[k]==0){
                        int sort[]={nums[i],nums[j],nums[k]};
                        for(int l=0; l<sort.length; l++){
                            for(int n=l+1; n<sort.length; n++){
                                if(sort[l]>sort[n]){
                                    int temp=sort[l];
                                    sort[l]=sort[n];
                                    sort[n]=temp;
                                }
                            }
                        }for(int m=0; m<sort.length; m++){
                            System.out.print(sort[m]+" ");
                        }  
                     System.out.print(",");}
                }
            }
        } System.out.print("]");
    }
    public static void main(String args[]){
        int nums[] = {-1, 0,  1, 2, -1, -4};
        returnTriplets(nums); 
    }
}

// Q.29 -> BUBBLE SORT.

import java.util.*;
public class JavaBasics{

    public static void bubbleSort(int arr[]){
        int n=arr.length;
        for(int turns=0; turns<n-2; turns++){
            for(int i=0; i<n-2-turns; i++){
                if(arr[i]>arr[i+1]){
                    int temp=arr[i];
                    arr[i]=arr[i+1];
                    arr[i+1]=temp;
                }
            }
        }for(int i=0; i<n; i++){
            System.out.print(arr[i]+" ");
        }
    }
    public static void main(String args[]){
        int arr[]={5,4,1,3,2,};
        bubbleSort(arr);
    }
}
// Q.30 -> SELECTION SORT.

import java.util.*;
public class JavaBasics{

    public static void selectionSort(int arr[]){
        for(int i=0; i<arr.length-1; i++){
            int minPos=i;
            for(int j=i+1; j<arr.length; j++){
                if(arr[minPos] > arr[j]){
                    minPos=j;
                }
            }int temp=arr[minPos];
                 arr[minPos]=arr[i];
                 arr[i]=temp;

        }for(int i=0; i<arr.length; i++){
            System.out.print(arr[i]+" ");
        }
        
    }
    public static void main(String args[]){
        int arr[]={5,4,1,3,2,};
        selectionSort(arr);
    }
}

// Q.31 -> COUNTING SORT.

import java.util.*;
public class JavaBasics{

    public static void countSort(int arr[]){
        int largest=Integer.MIN_VALUE;
        for(int i=0; i<arr.length; i++){
            largest = Math.max(largest,arr[i]);
        }int count[] = new int[largest+1];
        for(int j=0; j<arr.length; j++){
            int m=count[arr[j]]++;
            System.out.println(m);
        }int k=0;
        for(int i=0; i<count.length; i++){
            while(count[i]>0){
                arr[k]=i;
                k++;
                count[i]--;  
            }
        }for(int i=0; i<arr.length; i++){
            System.out.print(arr[i]+" ");
        }
    }
    public static void main(String args[]){
        int arr[] = {1,4,1,3,2,4,3,7};
        countSort(arr);
    }
}

// Q.32 -> INSERTION SORT.

import java.util.*;

public class JavaBasics {
    public static void Sort(int arr[]) {
    
        // Step 1: पहले एलिमेंट को सॉर्टेड मानकर 1st इंडेक्स से शुरू करें
        for (int i = 1; i < arr.length; i++) {
            int curr = arr[i]; // वर्तमान वैल्यू को सुरक्षित रखें
            int prev = i - 1;

            // Step 2: सही जगह ढूँढने के लिए पीछे के एलिमेंट्स से तुलना करें
            while (prev >= 0 && arr[prev] > curr) {
                arr[prev + 1] = arr[prev]; // बड़ी वैल्यू को आगे खिसकाएं
                prev--;
            }

            // Step 3: सही खाली जगह पर 'curr' को रख दें
            arr[prev + 1] = curr;
        }

        // आउटपुट प्रिंट करें
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }

    public static void main(String args[]) {
        int arr[] = {1, 4, 1, 3, 2, 4, 3, 7};
        Sort(arr);
    }
}

// Q.33 -> COUNT SORT.

import java.util.*;
public class JavaBasics{

    public static void countSort(int arr[]){
        int largest=Integer.MIN_VALUE;
        for(int i=0; i<arr.length; i++){
            largest=Math.max(largest,arr[i]);
        }
        int count[]=new int[largest+1];
        for(int i=0; i<arr.length; i++){
            count[arr[i]]++;
        }
        //sort
        int j=0;
        for(int i=0; i<count.length; i++){
            while(count[i]>0){
                arr[j]=i;
                j++;
                count[i]--;
            }
        }for (int i = 0; i < arr.length; i++) {
        System.out.print(arr[i] + " ");
        }
    }
    public static void main(String args[]){
        int arr[]={3,6,2,1,8,7,4,5,3,1};
        countSort(arr);
    }
}

// Q.34 -> TAKING SIZE, INPUT AND FINDING ELEMENT IN MATRIX OR 2D ARRAY.

import java.util.*;
public class JavaBasics{

    //FINDING ELEMENT IN MATRIX OR 2D ARRAY
    public static void searchMatrix(int matrix[][], int key){
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                 if(matrix[i][j]==key){
                 System.out.print("key found at cell ("+i+","+j+")");
                }
            }
        }
       
    }
    
    //TAKING INPUT IN MATRIX OR 2D ARRAY
    public static void inputMatrix(int matrix[][]){
        Scanner sc= new Scanner(System.in);
        System.out.print("enter matrix element:");
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                matrix[i][j]=sc.nextInt();
            }
        }
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        
        }
    }
    
    public static void main(String args[]){
        //TAKING SIZE OF MATRIX OR 2D ARRAY
        Scanner sc= new Scanner(System.in);
        System.out.print("enter size of matrix:");
        int n=sc.nextInt(); 
        int m=sc.nextInt();
        int matrix[][]= new int [n][m];
        inputMatrix(matrix);
        int key=5;
        searchMatrix(matrix,key);
    }
}

// Q.35 -> FINDING LARGEST ELEMENT IN MATRIX OR 2D ARRAY.

import java.util.*;
public class JavaBasics{

     //MAIN CODE FOR LARGEST ELT
    public static void largestInMatrix(int matrix [][]){
        int largest=Integer.MIN_VALUE;
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                largest=Math.max(largest,matrix[i][j]);
            }
        }System.out.println("largest elt is "+largest);

    }
    //TAKING INPUT IN MATRIX OR 2D ARRAY
    public static void inputMatrix(int matrix[][]){
        Scanner sc= new Scanner(System.in);
        System.out.print("enter matrix element:");
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                matrix[i][j]=sc.nextInt();
            }
        }
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        
        }
    }
    public static void main(String args[]){
        //TAKING SIZE OF MATRIX OR 2D ARRAY
        Scanner sc= new Scanner(System.in);
        System.out.print("enter size of matrix:");
        int n=sc.nextInt(); 
        int m=sc.nextInt();
        int matrix[][]= new int [n][m];
        inputMatrix(matrix);
        largestInMatrix(matrix);
    }
}

--------------------OR-------------------------

import java.util.*;

public class JavaBasics {

    // Pass the Scanner as a parameter to avoid creating multiple instances
    public static void inputMatrix(int[][] matrix, Scanner sc) {
        System.out.println("Enter matrix elements:");
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[0].length; j++) {
                matrix[i][j] = sc.nextInt();
            }
        }
    }

    public static void largestInMatrix(int[][] matrix) {
        // Correct logic: Start with the smallest possible integer
        int largest = Integer.MIN_VALUE;
        
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) { // Use matrix[i].length for safety
                largest = Math.max(largest, matrix[i][j]);
            }
        }
        System.out.println("Largest element is: " + largest);
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Enter size of matrix (rows and columns): ");
        int n = sc.nextInt(); 
        int m = sc.nextInt();
        
        int[][] matrix = new int[n][m];
        
        inputMatrix(matrix, sc);
        largestInMatrix(matrix);
        
        sc.close(); // Good practice to close the scanner when done
    }
}

// Q.36 -> FINDING SMALLEST ELEMENT IN MATRIX OR 2D ARRAY.

import java.util.*;
public class JavaBasics{

    public static void smallestInMatrix(int matrix [][]){
        int smallest=Integer.MAX_VALUE;
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                smallest=Math.min(smallest,matrix[i][j]);
            }
        }System.out.println("smallest elt is "+smallest);

    }
    //TAKING INPUT IN MATRIX OR 2D ARRAY
    public static void inputMatrix(int matrix[][]){
        Scanner sc= new Scanner(System.in);
        System.out.print("enter matrix element:");
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                matrix[i][j]=sc.nextInt();
            }
        }
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        
        }
    }
    public static void main(String args[]){
        //TAKING SIZE OF MATRIX OR 2D ARRAY
        Scanner sc= new Scanner(System.in);
        System.out.print("enter size of matrix:");
        int n=sc.nextInt(); 
        int m=sc.nextInt();
        int matrix[][]= new int [n][m];
        inputMatrix(matrix);
        smallestInMatrix(matrix);
    }
}

// Q.37 -> SPIRAL MATRIX PROBLEM.                                      [ ASKED IN GOOGLE, AMAZON, ORACLE, MICROSOFT, APPLE, ADOBE etc. ]        -->     IMPORATANT QUESTION

import java.util.*;
public class JavaBasics{

    public static void spiralMatrix(int matrix[][]){
        int startRow=0;
        int endRow=matrix.length-1;
        int startCol=0;
        int endCol=matrix[0].length-1;
        while(startRow<=endRow && startCol<=endCol){
            //top boundry
            for(int j=startCol; j<=endCol; j++){
                System.out.print(matrix[startRow][j]+" ");
            }
            //right boundry
            for(int i=startRow+1; i<=endRow; i++){
                System.out.print(matrix[i][endCol]+" ");
            }
            //bottom boundry
            for(int j=endCol-1; j>=startCol; j--){
                if(startRow==endRow){
                    break;
                }
                System.out.print(matrix[endRow][j]+" ");
            }
            //left boundry
            for(int i=endRow-1; i>=startRow+1; i--){
                if(startCol==endCol){
                    break;
                }
                System.out.print(matrix[i][startCol]+" ");
            }
            startRow++;
            endRow--;
            startCol++;
            endCol--;
        }
    }
    public static void main(String args[]){
        int matrix[][]={{1, 2, 3, 4},
                       {5, 6, 7, 8},
                       {9, 10,11,12},
                       {13,14,15,16}};
        spiralMatrix(matrix);               
    }
}

// Q.38 -> DIAGONAL SUM OF MATRIX.                                           [ ASKED IN GOOGLE, AMAZON, ORACLE, MICROSOFT, APPLE, ADOBE etc. ] 


------------------BRUTE FORCE SOLUTION { T.C = O(n^2) }-------------------
import java.util.*;
public class JavaBasics{

    public static void diagonalSum(int matrix[][]){
        int PDsum=0;
        int SDsum=0;
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                if(i==j){
                    PDsum = PDsum + matrix[i][j];
                }else if(i+j==matrix.length-1){
                    SDsum = SDsum + matrix[i][j];
                }
            }
        }System.out.println("\nPDsum,SDsum: "+PDsum+","+SDsum);
        int totSum = PDsum + SDsum;
        System.out.print("total diagonal sum: "+totSum);
    }
    public static void main(String args[]){
        int matrix[][]={{0,1,2},
                        {3,4,5},
                        {6,7,8}};
        diagonalSum(matrix);
    }
}

-----------------------OPTIMISE SOLUTION { T.C = O(n) }------------------------

import java.util.*;
public class JavaBasics{

    public static void diagonalSum(int matrix[][]){
        int PDsum=0;
        int SDsum=0;
        for(int i=0; i<matrix.length; i++){
            PDsum+=matrix[i][i];
            if(i!=matrix.length-1-i){
                //when i!=j then SDsum calculate karana hai, yha(j=matrix.length-1-i)
                SDsum+=matrix[i][matrix.length-1-i];
            }
        }
        System.out.println("\nPDsum,SDsum: "+PDsum+","+SDsum);
        int totSum = PDsum + SDsum;
        System.out.print("total diagonal sum: "+totSum);
    }
    public static void main(String args[]){
        int matrix[][]={{0,1,2},
                        {3,4,5},
                        {6,7,8}};
        diagonalSum(matrix);
    }
}












