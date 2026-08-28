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

-------------------ASSIGNMENT (FUNCTIONS QUESTIONS) ON FUNCTION & METHODS-----------------------

// Question 1 :Write a Java method to compute the average of three numbers. 

// Question2:Write a method named isEven that accepts an int argument. The method should return true if the argument is even, or false otherwise. Also write a program to test your method.

// Question3:Write a Java program to check if a number is a palindrome in Java? ( 121 is a palindrome, 321 is not) 
A number is called apalindrome if the number isequal to the reverse of a number e.g., 121 is a palindrome because the reverse of 121 is 121 itself.On the other hand, 321 is not a palindrome because the reverse of 321 is 123, which is not equal to 321.

// Question 4 :READ & CODE EXERCISE Search about(Google) & use the following methods of the Math class in Java: 
a.  Math.min( )
b.  Math.max( )
c.  Math.sqrt( )
d.  Math.pow( )
e.  Math.avg( )
f.  Math.abs( )
Free reading resource (https://www.javatpoint.com/java-math)
Please feel free to look for more resources/websites on your own.

// Question 5 :Write a Java method to compute the sum of the digits in an integer.

(Hint: Approach this question in the following way:
a. Take a variable sum = 0
b. Find the last digit of the number
c. Add it to the sum
d. Repeat a & b until the number becomes 0 )


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

// Q.35 ->SEARCH ( FINDING ELEMENT ) IN MATRIX / 2D ARRAY (UNSORTED).

import java.util.*;
public class JavaBasics{

    public static void searchMatrix(int matrix [][], int key){
        for(int row=0; row<matrix.length; row++){
            for(int col=0; col<matrix[0].length; col++){
                if(matrix[row][col]==key){
                    System.out.print("key is at: ("+row+","+col+")");
                    return;
                }
            }
        }
    }
    public static void main(String args[]){
        int matrix[][]={{10,20,30,40},
                        {15,25,35,45},
                        {27,29,37,48},
                        {32,33,39,50}};
        int key = 25;                
        searchMatrix(matrix,key);
    }
}


// Q.36 -> FINDING LARGEST ELEMENT IN MATRIX OR 2D ARRAY.

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

// Q.37 -> FINDING SMALLEST ELEMENT IN MATRIX OR 2D ARRAY.

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

// Q.38 -> SPIRAL MATRIX PROBLEM.                                      [ ASKED IN GOOGLE, AMAZON, ORACLE, MICROSOFT, APPLE, ADOBE etc. ]        -->     IMPORATANT QUESTION

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

// Q.39 -> DIAGONAL SUM OF MATRIX.                                           [ ASKED IN GOOGLE, AMAZON, ORACLE, MICROSOFT, APPLE, ADOBE etc. ] 


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

// Q.40 -> SEARCH ( FINDING ELEMENT ) IN SORTED MATRIX/2D ARRAY.                [ ASKED IN ORACLE ]  

import java.util.*;
public class JavaBasics{

    // TOP TO BOTTOM STAIRCASE SEARCH.
    public static void staircaseSearchTB(int matrix[][], int key){
        int row=0;
        int col=matrix[0].length-1;
        while(row<matrix.length && col>=0){
            if(matrix[row][col]==key){
                 System.out.print("key is at: ("+row+","+col+")");
                 return;
            }else if(matrix[row][col]>key){
                col--;
            }else {
                row++;
            }
        }System.out.print("key is not found");   
    }
    public static void main(String args[]){
        int matrix[][]={{10,20,30,40},
                        {15,25,35,45},
                        {27,29,37,48},
                        {32,33,39,50}};
        int key = 25;                
        staircaseSearchTB(matrix,key);
    }
}

------------------SAME BUT DIFFERENT APPROCH-------------------
import java.util.*;
public class JavaBasics{

    // BOTTOM TO TOP STAIRCASE SEARCH.
    public static void staircaseSearchBT(int matrix[][], int key){
        int row=matrix.length-1;
        int col=0;
        while( row>=0 && col<matrix[0].length){
            if(matrix[row][col]==key){
                 System.out.print("key is at: ("+row+","+col+")");
                 return;
            }else if(matrix[row][col]>key){
                row--;
            }else {
                col++;
            }
        }System.out.print("key is not found");   
    }
    public static void main(String args[]){
        int matrix[][]={{10,20,30,40},
                        {15,25,35,45},
                        {27,29,37,48},
                        {32,33,39,50}};
        int key = 10;                
        staircaseSearchBT(matrix,key);
    }
}

---------------------------------ASSIGNMENT (PRACTICE QUESTIONS) ON 2D ARRAY/MATRIX----------------------------

Question 1 :Print the number of 7’s that are in the 2d array.
Example :
Input - int[][] array = { {4,7,8},{8,8,7} };
Output - 2

Question 2 :Print out the sum of the numbers in the second row of the “nums” array.
Example :
Input - int[][] nums = { {1,4,9},{11,4,3},{2,2,3} };
Output - 18

Question 3 :Write a program to Find Transposeofa Matrix.What is Transpose?
Transpose of a matrix is the process ofswapping therows to columns. 
For a 2x3 matrix,
Matrix 
a11    a12    a13 
a21    a22    a23
Transposed Matrix
a11    a21
a12    a22
a13    a23


import java.util.*;
public class JavaBasics{

    // COUNTING OF GIVEN NUMBER IN MATRIX.
    public static void countNum(int matrix[][], int num){
        int count=0;
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                if(matrix[i][j]==num){
                    count++;
                }
            }
        }System.out.println("number "+num+" is: "+count);
    }

    // SUM OF THE NUMBERS IN Nth ROW OF MATRIX.
    public static void rowSum(int matrix[][], int row){
        int rowSum=0;
        for(int j=0; j<matrix[0].length; j++){
                    rowSum+=matrix[row-1][j];
        }System.out.println("sum of the numbers in "+row+" row is: "+rowSum);
    } 

    // SUM OF THE NUMBERS IN Nth COLUMN OF MATRIX.
    public static void colSum(int matrix[][], int col){
        int colSum=0;
        for(int i=0; i<matrix.length; i++){
                    colSum+=matrix[i][col-1];
        }System.out.println("sum of the numbers in "+col+" row is: "+colSum);
    } 

    // TRANSPOSE OF MATRIX.
    public static void transposeMatrix(int matrix[][]){
        int row=matrix.length; //row of given matrix
        int col=matrix[0].length; //col of given matrix
        int transpose[][]=new int[col][row];
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                transpose[j][i]=matrix[i][j];
            }                           
        }printMatrix(transpose);
    }

    // PRINT MATRIX (2D ARRAY).
    public static void printMatrix(int matrix[][]){
        for(int i=0; i<matrix.length; i++){
            for(int j=0; j<matrix[0].length; j++){
                System.out.print(matrix[i][j]+" ");
            }System.out.println();                           
        }
    }

    
    public static void main(String args[]){
        int matrix[][]={{1,5,9},
                        {2,4,3}};
        int num = 7;
        countNum(matrix,num);
        int row = 2;
        rowSum(matrix,row);
        int col = 1;
        colSum(matrix,col);
        transposeMatrix(matrix);
    }
}

----------------------------------------STRINGS------------------------------------------------

// Q.41 -> CHECK IF STRING IS PALINDROME.

----------------BRUTE FORCE-----------------
import java.util.*;
public class JavaBasics{

    public static void Palindrome(String str){
        String str1="";
        for(int i=str.length()-1; i>=0; i--){
            char str2=str.charAt(i);
            str1=str1+str2;
        }
        if(str1.equals(str)){
            System.out.println("String '"+str+"' is Palindrome.");
        }else{
            System.out.println("String '"+str+"' is not Palindrome.");
        }
    }
    public static void main(String args[]){
        String str="madam";
        Palindrome(str);
    }
}

-------------------OPTIMISED-------------------
import java.util.*;
public class JavaBasics{

    public static boolean isPalindrome(String str){
        for(int i=0; i<str.length()/2; i++){
            int n=str.length();
            if(str.charAt(i) != str.charAt(n-1-i)){
                //not a palindrome
                return false;
            }
        }return true;
        
    }
    public static void main(String args[]){
        String str="madam";
        System.out.println(isPalindrome(str));;
    }
}

// Q.42 -> SHORTEST PATH OF GIVEN ROUTE CONTAINING 4 DIRECTIONS (E,W,N,S).

import java.util.*;
public class JavaBasics{

    public static double getShortestPath(String path, int x1, int y1){
        //x1,y1 is starting point
        int x=0, y=0;
        for(int i=0; i<path.length(); i++){
            char dir=path.charAt(i);
            if(dir=='E'){
                x++;
            }else if(dir=='W'){
                x--;
            }else if(dir=='N'){
                y++;
            }else{
                y--;
            }
        }double shortestPath = Math.sqrt((x-x1)*(x-x1) + (y-y1)*(y-y1));
        return shortestPath;
    }
    public static void main(String args[]){
        String path="NS";
        //starting point
        int x1=0,y1=0;
        System.out.println("shortest path is: "+getShortestPath(path,x1,y1));
    }
}

// Q.43 -> SUBSTRING OF GIVEN STRING.

-----INBUILT SUBSTRING FUNCTION { str.substring(si,ei) }---------
import java.util.*;
public class JavaBasics{

    public static String substring(String str, int si, int ei){
        String substr="";
        for(int i=si; i<ei; i++){
            substr+=str.charAt(i);
        }
        return substr;
    }
    public static void main(String args[]){
        String str = "Hello World";
        int si=3, ei=5;
        System.out.print(substring(str,si,ei));
    }
}

// Q.44 -> PRINT LARGEST (LEXICOGRAPHIC) STRING FROM GIVEN SET OF STRING.

import java.util.*;
public class JavaBasics{

    //USE str1.comparToIgnoreCase FOR 'A'='a' MEANS NO DIFFERENCE IN UPPER CASE AND LOWER CASE LETTERS
    public static String largestString(String str[]){
        String largest=str[0];
        for(int i=1; i<str.length; i++){
            if(largest.compareTo(str[i])<0){
                largest=str[i];
            }
        }return largest;
    }
    public static void main(String args[]){
        String str[] = {"apple","mango","banana"};
        System.out.print(largestString(str));
    }
}

// Q.45 -> CONVERT EACH FIRST LETTER OF EACH WORD TO UPPER CASE.           { ASKED IN <CODE_NATION> }
import java.util.*;
public class JavaBasics{

    public static String toUpperCase(String str){
        StringBuilder sb = new StringBuilder("");
        char ch = Character.toUpperCase(str.charAt(0));
        sb.append(ch);

        for( int i=1; i<str.length(); i++){
            if(str.charAt(i) == ' ' && i<str.length()-1){
                sb.append(str.charAt(i));
                i++;
                sb.append(Character.toUpperCase(str.charAt(i)));
            }else{
                sb.append(str.charAt(i));
            }
        }return sb.toString();
    }
    public static void main(String args[]){
        String str = "hi, i am nikhil";
        System.out.print(toUpperCase(str));
    }
}

// Q.46 -> STRING COMPRESSION.                                  { ASKED IN AMAZON --- MOST COMMON QUESTION }
import java.util.*;
public class JavaBasics{

     //---------USING STRING BUILDER (OPTIMIZED)---------
    public static String compress(String str){
        StringBuilder newStr= new StringBuilder("");
        for(int i=0; i<str.length(); i++){
            Integer count=1;
            while(i<str.length()-1 && str.charAt(i)==str.charAt(i+1)){
                count++;
                i++;
            }
            newStr.append(str.charAt(i));
            if(count > 1){
                newStr.append(count); // you can use newStr.append(count.toString()); but it is inefficient.
            }
        }return newStr.toString();
    }
    
    //---------WITHOUT STRING BUILDER---------
    public static String Compress(String str){
        String newStr= new String("");
        for(int i=0; i<str.length(); i++){
            Integer count=1;
            while(i<str.length()-1 && str.charAt(i)==str.charAt(i+1)){
                count++;
                i++;
            }
            newStr+=str.charAt(i);
            if(count > 1){
                newStr+=count.toString();// you can use newStr+=count; it is safer for NULL handling but inefficient.
            }
        }return newStr;
    }
    public static void main(String args[]){
        String str="aaabbcccdd";
        System.out.println(compress(str));
        System.out.println(Compress(str));
    }
}

// Q.47 -> COUNT LOWERCASE VOWEL.
import java.util.*;
public class JavaBasics{

    public static int countLowercaseVowel(String str){
        int count=0;
        for(int i=0; i<str.length(); i++){
            char ch = str.charAt(i);
            if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'){
                count++;
            }
        }return count;
    }
    public static void main(String args[]){
        System.out.print("Enter your String: ");
        String str= new Scanner(System.in).nextLine();
        //Scanner sc= new Scanner(System.in);
        //String str=sc.nextLine();
        System.out.println("no of vowel in your entered String is: "+countLowercaseVowel(str));
    }
}

----------------STRING QUESTIONS (ASSIGNMENT)-------------------

// Q.48 -> CHECK ANAGRAMS.
What are anagrams?
If two strings contain the same characters but in a different order, they can be said to be anagrams.Consider race andc are.

import java.util.*;
public class JavaBasics{

    public static void checkAnagrams(String str1, String str2){
        str1 = str1.toLowerCase();
        str2 = str2.toLowerCase();
        if(str1.length()==str2.length()){
            // String ko Array me convert kiya
            char[] str1CharArray = str1.toCharArray();
            char[] str2CharArray = str2.toCharArray();
            // String Array ko sort kiya
            Arrays.sort(str1CharArray);
            Arrays.sort(str2CharArray);

            boolean result = Arrays.equals(str1CharArray,str2CharArray);
            if(result){
                System.out.println(str1+" and "+str2+" are anagrams of eachother.");
            }else{
                System.out.println(str1+" and "+str2+" are not anagrams of eachother.");
            }
        }else{
            System.out.println(str1+" and "+str2+" are not anagrams of eachother.");
        }
    }
    public static void main(String args[]){
        String str1="earth", str2="heart";
        checkAnagrams(str1,str2);
    }
}

----------------------------------------BIT_MANIPULATION------------------------------------------------

// Q.49 -> CHECK FOR ODD OR EVEN.

import java.util.*;
public class JavaBasics{

    public static void oddOrEven(int n){
        //int bitMask=1;
        //if((n & bitMask)==0) you can also use this
        if((n&1)==0){
            System.out.println(n+" is Even number");
        }else{
            System.out.println(n+" is Odd number");
        }
    }
    public static void main(String args[]){
        System.out.print("Enter ur number: ");
        int n = new Scanner(System.in).nextInt();
        oddOrEven(n);
    }
}

// Q.50 -> GET iTH BIT.

import java.util.*;
public class JavaBasics{

    public static int getIthBit(int n, int i){
        int bitMask =1 << i;
        if((n & bitMask)==0){
            return 0;
        }else{
            return 1;
        }
    }
    public static void main(String args[]){
        System.out.print("Enter ur number: ");
        int n = new Scanner(System.in).nextInt();
        System.out.print("Enter ur i: ");
        int i = new Scanner(System.in).nextInt();
        System.out.print(i+"th bit is: "+getIthBit(n,i));
    }
}

// Q.51 -> SET iTH BIT.

import java.util.*;
public class JavaBasics{

    public static int setIthBit(int n, int i){
        int bitMask =1 << i;
        return (n | bitMask);
    }
    public static void main(String args[]){
        System.out.print("Enter ur number: ");
        int n = new Scanner(System.in).nextInt();
        System.out.print("Enter ur i: ");
        int i = new Scanner(System.in).nextInt();
        System.out.print(i+"th bit is: "+setIthBit(n,i));
    }
}


// Q.52 --> UPDATE iTH BIT. { MORE ELEGENT }

import java.util.*;
public class JavaBasics{

    public static int clearIthBit(int n, int i){
        int bitMask = ~(1<<i);
        return n & bitMask;
    }

    public static int updateIthBit(int n, int i, int newBit){
        n = clearIthBit(n,i);
        int BitMask = (newBit << i);
        return n | BitMask;
    }

    public static void main(String args[]){
        int n = 10;
        int i = 2;
        int newBit = 1;
        System.out.println(i+"th bit updated to: "+updateIthBit(n,i,newBit));
    }
}


// Q.53 --> SET, CLEAR, UPDATE iTH BIT.

import java.util.*;
public class JavaBasics{

    public static int setIthBit(int n, int i){
        int bitMask =(1 << i);
        return (n | bitMask);
    }

    public static int clearIthBit(int n, int i){
        int bitMask = ~(1<<i);
        return n & bitMask;
    }

    public static int updateIthBit(int n, int i, int newBit){
        if(newBit == 0){
            return clearIthBit(n,i);
        }else{
            return setIthBit(n,i);
        }
    }
    public static void main(String args[]){
        int n = 10;
        int i = 2;
        int newBit = 0;
        System.out.println(i+"th bit set to: "+setIthBit(n,i));
        System.out.println(i+"th bit cleared to: "+clearIthBit(n,i));
        System.out.println(i+"th bit updated to: "+updateIthBit(n,i,newBit));
    }
}

// Q.54 -->  CLEAR I BITS.

import java.util.*;
public class JavaBasics{

    public static int clearIBits(int n, int i){
        int bitMask = (~0)<<i;
        return n & bitMask;
    }

    public static void main(String args[]){
        int n = 15;
        int i = 2;
        System.out.println(i+"th bit updated to: "+clearIBits(n,i));
    }
}

// Q.55 -->  CLEAR BITS IN RNAGE.

import java.util.*;
public class JavaBasics{

    public static int clearBitsRange(int n, int i, int j){
        int a = (~0)<<(j+1);
        int b = (1<<i) -1;
        int bitMask = a | b;
        return n & bitMask;
    }

    public static void main(String args[]){
        int n = 2515;
        int i = 2;
        int j = 7;
        System.out.println("bits are cleared from "+i+" to "+j+" and ans is: "+clearBitsRange(n,i,j));
    }
}

// Q.56 --> NUMBER IS POWER OF TWO OR NOT.

import java.util.*;
public class JavaBasics{

     public static boolean isPowerOfTwo(int n){
        return (n & (n-1))==0;
    }


    public static void main(String args[]){
        int n = 5;
        System.out.println("is "+n+" Power Of Two: "+isPowerOfTwo(n));
    }    
}

// Q.57 --> COUNT SET BITS IN A NUMBER.

import java.util.*;
public class JavaBasics{

    //FOR +VE NUMBERS 
    public static int countSetBits(int n){
        int count = 0;
        while(n>0){
            if((n&1) != 0){
                count++;
            }
            n=(n>>1);
        }return count;
    }


    public static void main(String args[]){
        int n = 10;
        System.out.println("no of set bits is: "+countSetBits(n));
    }    
}

// Q.58 --> FAST EXPONENTIATION.

import java.util.*;
public class JavaBasics{

    public static int fastExponentiation(int a, int n){
        int ans = 1;
        while(n>0){
            if((n&1) != 0){//check LSB
                ans = ans*a;
            }
            a=a*a;
            n=n>>1;
        }
        return ans;
    }
    public static void main(String args[]){
        System.out.print(fastExponentiation(3,5));
    }
}

// Q.59 --> MODULAR EXPONENTIATION.             { ASKED IN GOOGLE }  

import java.util.*;
public class JavaBasics{

    public static long modularExponentiation(long base, long exp, long mod) {
       long res = 1;
       base = base % mod; // Initial reduction
       while (exp > 0) {
            // If current bit is 1, multiply base to result
             if ((exp & 1) == 1) res = (res * base) % mod;
        
            // Square the base for the next bit position
             base = (base * base) % mod;
        
            // Move to the next bit in the exponent
             exp >>= 1;
        }
        return res;
    }

    public static void main(String args[]){
        System.out.println(modularExponentiation(3,5,5));
    }

}

---------------------------------------BIT MANIPULATION QUESTIONS (ASSIGNMENT)--------------------------------------

// Q.60 --> WHAT IS THE VALUE OF X^X FOR ANY VALUEOF X?

THE VALUE OF X^X = 0.
THINK ABOUT IT,XOR GIVES 0 WHEN THE BITS ARE THE SAME.IF WE COMPARE THE SAME NUMBER TO ITSELF, THE BITS WILL ALWAYS BE THE SAME. SO, THE ANSWER OF X^X WILL ALWAYS BE 0


// Q.61 --> SWAP TWO NUMBERS WITHOUT USING ANY THIRD VARIABLE.

import java.util.*;
public class JavaBasics{

    public static void swapXor(int a, int b){
        System.out.println("(a,b) before swaping: ("+a+","+b+")");
        a = a^b;
        b = a^b;
        a = a^b;
        System.out.println("(a,b) after swaping: ("+a+","+b+")");
    }
    public static void main(String args[]){
        int a=2;
        int b=5;
        swapXor(a,b);
    }
}

// Q.62 --> ADD 1 TO AN INTEGER USING BIT MANIPULATION.  (HINT: TRY USING BITWISE NOT OPERATOR).

import java.util.*;
public class JavaBasics{

    public static int addOneBitwise(int n){
        // -(~n)=n+1 bcz (~x = -x-1) 
        return -~n;
    } 
    
    public static void main(String args[]){
        System.out.println(addOneBitwise(6));
    }
}

// Q.63 --> UPPERCASE TO LOWERCASE.

import java.util.*;
public class JavaBasics{

    // USING BITWISE OPERATER 
    public static char UppercaseToLowercase(char ch){
        char lowercase = ((char)(ch | ' '));
        return lowercase;
    }

    public static void main(String args[]){
        char ch = 'G';
        System.out.println(UppercaseToLowercase(ch));    
    }
}

// Q.64 --> LOWERCASE TO UPPERCASE.

import java.util.*;
public class JavaBasics{

    // USING BITWISE OPERATER 
    public static char UppercaseToLowercase(char ch){
        char lowercase = ((char)(ch & '_'));
        return lowercase;
    }

    public static void main(String args[]){
        char ch = 'g';
        System.out.println(UppercaseToLowercase(ch));    
    }
}

// Q. --> A GOOD READ OF HACKS USING BITS (YOU CAN CHECK THIS OUT IN YOUR FREE TIME) :

https://graphics.stanford.edu/~seander/bithacks.html


-------------------------------------------OOPS------------------------------------------------

// Q. --> METHOD OVERLOADING.

public class OOPS{

    public static void main(String args[]){
        Calculator calc=new Calculator();
        System.out.println(calc.sum(1,2));
        System.out.println(calc.sum((float)1.5,(float)2.2));
        System.out.println(calc.sum(1,2,5));
    }
}

class Calculator{

    int sum(int a, int b){
        return a+b;
    }
    float sum(float a, float b){
        return a+b;
    }
    int sum(int a, int b, int c){
        return a+b+c;
    }
}

// Q. --> METHOD OVERRIDING.

import java.util.*;
public class OOPS{

    public static void main(String args[]){
        Deer d = new Deer();
        d.eat();
    }
}
class Animal{

    void eat(){
        System.out.println("eat everything");
    }
}
class Deer extends Animal{

    void eat(){
        System.out.println("eats grass");
    }
}

-----------------------ASSIGNMENT QUESTIONS {OOPS}--------------------------

// Q.65 --> PRINT THE SUMM, DIFFERENCE AND PRODUCT OF TWO COMPLEX NUMBER BY CREATING A CLASS NAMED 'COMPLEX' WITH SEPERATE METHODS FOR EACH OPERATION WHOSE REAL AND IAMGINARY PART ARE ENETERED BY USER.

---------------------BRUTE FORCE---------------------
import java.util.*;
public class OOPS{

    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter ur real part of complex number: ");
        double c =sc.nextDouble();
        System.out.print("Enter ur imaginary part of complex number: ");
        double d =sc.nextDouble();
        System.out.print("Enter ur real part of complex number: ");
        double e =sc.nextDouble();
        System.out.print("Enter ur imaginary part of complex number: ");
        double f =sc.nextDouble();
        Complex cmplx= new Complex();
        cmplx.sum(c,d,e,f);
        cmplx.difference(c,d,e,f);
        cmplx.product(c,d,e,f);
    }
}
class Complex{

    public void sum(double c, double d,double e, double f){
        double a=c+e;
        double b=d+f;
        System.out.println(a+","+b+"i");
    }
    public void difference(double c, double d,double e, double f){
        double a=c-e;
        double b=d-f;
        System.out.println(a+","+b+"i");
    }
    public void product(double c, double d,double e, double f){
        double a = c*e - d*f;        
        double b = c*f + d*e;
        System.out.println(a+","+b+"i");
    }
}

---------------OR------------------

import java.util.*;
public class OOPS{

    public static void main(String args[]){
        Complex c=new Complex(4,5);
        Complex d=new Complex(9,4);
        
        Complex e=Complex.add(c,d);
        Complex f=Complex.diff(c,d);
        Complex g=Complex.product(c,d);
        
        e.printComplex();
        f.printComplex();
        g.printComplex();
    }
}
class Complex{
    int real;
    int imag;
    
    public Complex(int r,int i){
        real=r;
        imag=i;
    }
    
    public static Complex add(Complex a,Complex b){
        return new Complex((a.real+b.real),(a.imag+b.imag));
    }
    public static Complex diff(Complex a,Complex b){
        return new Complex((a.real-b.real),(a.imag-b.imag));
    }
    public static Complex product(Complex a,Complex b){
        return new Complex(((a.real*b.real)-(a.imag*b.imag)),((a.real*b.imag)+(a.imag*b.real)));
    }
    
    public void printComplex(){
        if(real==0 && imag!=0){
            System.out.println(imag+"i");
        }else if(real!=0 && imag==0){
            System.out.println(real);
        }else{
            System.out.println(real+"+"+imag+"i");
        }
    }
}

// Q.66 --> WHAT IS THE OUTPUT OF THE FOLLOWING PROGRAM?
class Automobile{

    private String drive(){
        return "Driving vehicle";
    }
}
class Car extends Automobile{

    protected String drive(){
        return "Driving vehicle";
    }
}
public class ElectricCar extends Car{

    public final String drive() {
        return "Driving electric car";
    }

    public static void main(String[] wheels) {
        final Car car = new ElectricCar();
        System.out.print(car.drive());
    }
}

A. Driving vehicle
B. Driving electric car
C. Driving car
D. The code does not compile

//HAVE COMPILATION ERROR ->  FILE NAME = PUBLIC CLASS NAME ,ELSE PRINT -> (B) DRIVING ELECTRIC CAR

// Q.67 -->  LOOK AT THE FOLLOWING CODE AND CHOOSETHE RIGHT OPTION FOR THE WORD:
//Shape.java
public class Shape{

    protected void display(){
        System.out.println("Display-base");
    }
}
//Circle.java
public class Circle extends Shape{

     <access modifiers> void display(){
        System.out.println("Display-base");
    }
}
a. Only protected can be used.
B. public and protected both can be used.
C. public, protected, and private can be used.
d. Only public can be used.
// ANS-B (JAVA DOES NOT ALLOW TO REDUCE THE VISIBILITY OF THE INHERITED METHOD,  default AND private WILL REDUCE THE VISIBILITY OF THE INHERITED METHOD).

// Q.68 --> WHAT IS THE OUTPUT OF THE FOLLOWING PROGRAM?
abstract class Car{

    //satic initialization block
    static{
        System.out.println("1");
    }
    public Car(String name){
        super();
        System.out.println("2");
    }
    //instance initialization block
    {
        System.out.println("3");
    }
}
public class BlueCar extends Car{

    //instance initialization block
    {
        System.out.println("4");
    }
    public BlueCar(){
        super("blue");
        System.out.println("5");
    }

    public static void main(String gears[]){
        new BlueCar();
    }
}
A. 23451
B. 12354
C. 13245
D. The code does not compile.
//ANS-C (Theclass is loaded first,with the static initialization block called and 1 is outputted
first. When the BlueCar is created in the main() method, the super class initialization
happens first. The instance initialization blocks are executed before the constructor,
so 32 is outputted next. Finally, the class is loaded with the instance initialization
blocks again being called before the constructor, outputting 45. The result is that
13245 is printed, making Option C the correct answer.)


// TASK --> READ UP ABOUT BASICS OF EXCEPTION HANDLING FROM HERE.
https://www.w3schools.com/java/java_try_catch.asp

-------------------------------------------RECURSION BASICS (PART 1)-------------------------------------------

// Q.69 --> PRINT NUMBER SFROM N TO 1 (DECREASING ORDER) USING RECURSION.

public class RecursionBasics{
          
    public static void printDecreasing(int n){
        if(n==1){
            System.out.print(n);
            return;
        }
        System.out.print(n+" ");
        printDecreasing(n-1);
    }
  
    public static void main(String args[]){
        printDecreasing(5);
    }
}

// Q.70 --> PRINT NUMBER SFROM 1 TO N (INCREASING ORDER) USING RECURSION.

public class RecursionBasics{

    public static void printIncreasing(int n){
        if(n==1){
            System.out.print(n+" ");
            return;
        }
        printIncreasing(n-1);
        System.out.print(n+" ");
    }
    public static void main(String args[]){
        printIncreasing(5);
    }
}

// Q.71 --> PRINT FACTORIAL OF A NUMBER N USING RECURSIN.

public class RecursionBasics{

    public static int factorial(int n){
        if(n==0){
          return 1;
        }
        return n*factorial(n-1);
    }
    public static void main(String args[]){
        System.out.println(factorial(5));
    }
}

// Q.72 --> PRINT SUM OF FIRST N NATURAL NUMBERS USING RECURSIN.

public class RecursionBasics{

    public static int printFNNsum(int n){
        if(n==1){
            return 1;
        }
        return n+printFNNsum(n-1);
    }
    public static void main(String args[]){
        System.out.print(printFNNsum(6));
    }
}

// Q.73 --> PRINT Nth FIBONACCI NUMBER USING RECURSION.

public class RecursionBasics{

    public static int printNthFibonacci(int n){
        if(n==0 || n==1){
            return n;
        }
        return printNthFibonacci(n-1)+printNthFibonacci(n-2);
    }
    public static void main(String args[]){
        System.out.println(printNthFibonacci(5));
    }
}

// Q.74 --> CHECK IF A GIVEN ARRAY IS SORTED (ASCENDING ORDER) OR NOT USING RECURSION.

public class RecursionBasics{

    public static boolean isSorted(int arr[],int i){
        if(i == arr.length-1){
            return true;
        }
        if(arr[i] > arr[i+1]){
            return false;
        }
        return isSorted(arr,i+1);
    }
    public static void main(String args[]){
        int arr[]={1,2,3,3,4,5};
        System.out.println(isSorted(arr,0));
    }
}

// Q.75 --> WAF TO FIND THE FIRST OCCURENCE OF AN ELEMENT IN AN ARRAY USING RECURSION.

public class RecursionBasics{

    public static int firstOccurence(int arr[], int target,int i){

        if(i==arr.length){
            System.out.println("element not found");
            return -1;
        }
        if(arr[i]==target){
            return i;
        }
        return firstOccurence(arr,target,i+1);
    }
    public static void main(String args[]){
        int arr[]={1,2,3,4,4,5};
        System.out.println("element is at position "+firstOccurence(arr,5,0)+" at first occurence");
    }
}

// Q.76 --> WAF TO FIND THE LAST OCCURENCE OF AN ELEMENT IN AN ARRAY USING RECURSION.

public class RecursionBasics{

    public static int lastOccurance(int arr[],int target, int i){
        if(i==arr.length){
            return -1;
        }
        int isFound = lastOccurance(arr,target,i+1);
        if(isFound==-1 && arr[i]==target){
            return i;
        }
        return isFound;
    }
    public static void main(String args[]){
        int arr[]={8,3,6,9,5,10,2,5,3};
        System.out.println(lastOccurance(arr,5,0));
    }
}

// Q.77 --> WAF TO CALCULATE POWER OF A NUMBER USING RECURSION.

public class RecursionBasics{

    public static int power(int x,int n){
        if(n==0){
            return 1;
        }
        return x*power(x,n-1);
    }

    public static void main(String args[]){
        System.out.println(power(2,5));
    }
}

// Q.78 --> WAF TO CALCULATE POWER OF NUMBER IN O(logn) USING RECURSION.

public class RecursionBasics{

    // T.C = O(logn)
    public static int power(int base, int pow){
        if(pow==0){
            return 1;
        }
        // agr {int halfPowerSq = power(n,pow/2)*power(n,pow/2);} --> T.C=O(n) dega
        int halfPower=power(base,pow/2);
        int halfPowerSq = halfPower*halfPower;
        if(pow%2!=0){
            halfPowerSq = base*halfPowerSq;
        }
        return halfPowerSq;
    }
    public static void main(String args[]){
        System.out.println(power(2,10));
    }
}

// Q.79 --> Tiling Problem
Given a "2 x n" floor and tiles of size "2 x 1", count the number of
ways to tile the given floor using the 2 x 1 tiles.
(A tile can either be placed horizontally or vertically. )

public class RecursionBasics{

    public static int tilingProblem(int n){
        if(n==0 || n==1){
            return 1;
        }
        //verticle ways
        int fnm1=tilingProblem(n-1);
        //horizontal ways
        int fnm2=tilingProblem(n-2);
        return fnm1+fnm2;
    }
    public static void main(String args[]){
        System.out.println(tilingProblem(3));
    }
}

// Q.80 --> WAF TO REMOVE DUPLICATES IN A STRING USING RECURSION.

public class RecursionBasics{

    public static void removeDuplicates(String str,int index, StringBuilder newStr, boolean map[]){
        if(index==str.length()){
            System.out.println(newStr);
            return;
        }
        char currChar = str.charAt(index);
        if(map[currChar-'a'] == true){
            //duplicate found
            removeDuplicates(str,index+1,newStr,map);
        }else{
            map[currChar-'a'] = true;
            removeDuplicates(str,index+1,newStr.append(currChar),map);
        }
    }
    public static void main(String args[]){
        removeDuplicates("appnnacollege",0,new StringBuilder(""),new boolean[26]);
    }
}

// Q.81 --> Friends Pairing Problem
Given n friends, each one can remain single or can be paired up with some other
friend. Each friend can be paired only once. Find out the total number of ways in
which friends can remain single or can be paired up.

public class RecursionBasics{

    public static int friendsPairing(int n){
        if(n==1 || n==2){
            return n;
        }
        return friendsPairing(n-1) + (n-1)*friendsPairing(n-2);
    }
    public static void main(String args[]){
        System.out.print(friendsPairing(3));
    }
}

// Q.82 --> BINARY STRING PROBLEM: PRINT ALL BINARY STRING OF SIZE N WITHOUT CONSECUTIVE ONE USING RECURSION.

public class RecursionBasics{

    public static void printBinary(int n,int lastPlace,String str){
        if(n==0){
            System.out.println(str);
            return;
        }
        printBinary(n-1,0,str+"0");
        if(lastPlace == 0){
            printBinary(n-1,1,str+"1");
        }
    }
    public static void main(String args[]){
        printBinary(2,0,"");
    }
}
// Q.83 --> BINARY STRING PROBLEM: PRINT ALL BINARY STRING OF SIZE N WITHOUT CONSECUTIVE ZERO USING RECURSION.

public class RecursionBasics{

    public static void printBinary(int n,int lastPlace,String str){
        if(n==0){
            System.out.println(str);
            return;
        }
        printBinary(n-1,1,str+"1");
        if(lastPlace == 1){
            printBinary(n-1,0,str+"0");
        }
    }
    public static void main(String args[]){
        printBinary(2,1,"");
    }
}

--------------------------------------ASSIGNMENT QUESTIONS (RECURSION BASICS)-------------------------------------

Question 1 : For a given integer array of size N. You have to find all the occurrences
(indices) of a given element (Key) and print them. Use a recursive function to solve this
problem.
Sample Input : arr[ ] = {3, 2, 4, 5, 6, 2, 7, 2, 2}, key = 2
Sample Output : 1 5 7 8

public class RecursionBasics{

    public static void allOccurence(int arr[],int i,int key){
        if(i==arr.length){
            System.out.println("\nif it is empty then the key is not in the array");
            return;
        }
        if(arr[i]==key){
            System.out.print(i+" ");
        }
        allOccurence(arr,i+1,key);
    }
    public static void main(String args[]){
        int arr[] = {3, 2, 4, 5, 6, 2, 7, 2, 2};
        allOccurence(arr,0,9);
        System.out.println();
    }
}
---------------------------0R-----------------------------

public class RecursionBasics{

    //(USER CENTRIC)
    public static boolean allOccurence(int arr[],int i,int key,boolean found){
        if(i==arr.length){
            return found;
        }
        if(arr[i]==key){
            System.out.print(i+" ");
            found=true;
        }
        return allOccurence(arr,i+1,key,found);
    }
    public static void main(String args[]){
        int arr[] = {3, 2, 4, 5, 6, 2, 7, 2, 2};
        boolean isFound=allOccurence(arr,0,9,false);
        if(!isFound){
            System.out.print("-1 ");
        }
        System.out.println();
    }
}

Question 2 :
You are given a number (eg -  2019), convert it into a String of english like
“two zero one nine”.  Use a recursive function to solve this problem.
NOTE- The digits of the number will only be in the range 0-9 and the last digit of a number
can’t be 0.
Sample Input : 1947
Sample Output : “one nine four seven”

public class RecursionBasics{

    //NUMBER TO STRING(MY SOLUTION)
    public static void numToString(int n){
        if(n==0){
            return;
        }
        numToString(n/10);
        System.out.print(getString(n%10)+" ");
    }
    public static String getString(int n){
        switch(n){
            case 0:return "zero";
            case 1:return "one";
            case 2:return "two";
            case 3:return "three";
            case 4:return "four";
            case 5:return "five";
            case 6:return "six";
            case 7:return "seven";
            case 8:return "eight";
            case 9:return "nine";
            default:return "NA";
        }
    }
    public static void main(String args[]){
        numToString(2019);
    }
}
--------------------------------OR--------------------------------

public class RecursionBasics{
    
    //ANOTHER SOLUTION (NOT MINE)
    static String digits[]={"zero","one","two","three","four","five","six","seven","eight","nine"};
    public static void numToString(int n){
        if(n==0){
            return;
        }
        numToString(n/10);
        System.out.print(digits[n%10]+" ");
    }

    public static void main(String args[]){
        numToString(2019);
    }
}

Question 3 : Write a program to find Length of a String using Recursion.

public class RecursionBasics{

    //LENGTH OF STRING(MY SOLUTION)
    public static int stringLength(String str,int i){
        if(i==str.length()){
            return i;
        }
        return stringLength(str,i+1);
    }
    public static void main(String args[]){
        System.out.println(stringLength("Nikhil",0));
    }
}
----------------------OR-----------------------

public class RecursionBasics{

    //LENGTH OF STRING(NOT MINE)
    public static int stringLength(String str){
        if(str.length()==0){
            return 0;
        }
        return stringLength(str.substring(1))+1;
    }
    public static void main(String args[]){
        System.out.println(stringLength("Nikhil"));
    }
}

Question 4 : We aregivenastring S, weneedto find the count of all contiguous substrings
starting and ending with the same character.
Sample Input 1 : S = "abcab"
Sample Output 1 : 7
There are 15 substrings of "abcab" : a, ab, abc, abca, abcab, b, bc, bca, bcab, c, ca, cab, a, ab, b
Out of the above substrings, there are 7 substrings : a, abca, b, bcab, c, a and b. So, only 7
contiguous substrings start and end with the same character.
Sample Input 2 : S = "aba"
Sample Output 2 : 4
The substrings are a, b, a and aba

public class RecursionBasics{

    public static int countSubstrs(String str, int i, int j, int n){
        if (n == 1){
            return 1;
        }
        if (n <= 0){
            return 0;
        }

        int res = countSubstrs (str, i + 1, j, n - 1) +
        countSubstrs (str, i, j - 1, n - 1) -
        countSubstrs(str, i + 1, j - 1, n - 2);

        if (str.charAt (i) == str.charAt (j)){
            res++;
        }

        return res;
    }



    public static void main(String[] args){
        String str = "aba";
        int n= str.length ();
        System.out.print(countSubstrs(str, 0, n-1, n));
    }

}

-----------------------OR------------------------

public class RecursionBasics {

    public static int countSubstrings(String str, int i, int j) {
        // Base Case 1: If starting index reaches the end, we are done
        if (i == str.length()) {
            return 0;
        }
        
        // Base Case 2: If ending index goes out of bounds, move to the next starting character
        if (j == str.length()) {
            return countSubstrings(str, i + 1, i + 1);
        }
        
        // Check if the current substring str.substring(i, j+1) starts and ends with the same char
        int match = (str.charAt(i) == str.charAt(j)) ? 1 : 0;
        
        // Move to the next ending index 'j' and add the result
        return match + countSubstrings(str, i, j + 1);
    }

    public static void main(String[] args) {
        String str = "aba";
        // Start both i and j at 0
        int totalCount = countSubstrings(str, 0, 0); 
        System.out.println("Total matching substrings: " + totalCount); // Output: 7
    }
}

Question 5 : TOWER OF HANOI(Important!)

You have 3 towers and N disks of different sizes which can slide onto any tower. The puzzle
starts with disks sorted in ascending order of size from top to bottom (i.e., each disk sits on
top of an even larger one).
You have the following constraints:
(1) Only one disk can be moved at a time.
(2) A disk is slid off the top of one tower onto another tower.
(3) A disk cannot be placed on top of a smaller disk. Write a program to move the disks from
the first tower to the
last using Recursion/Stacks.

Let rod 1 = 'A', rod 2 = 'B', rod 3 = 'C'.

An example with 2 disks i.e. N=2:
Step 1 : Shift the first disk from 'A' to 'B'.
Step 2 : Shift the second disk from 'A' to 'C'.
Step 3 : Shift the first disk from 'B' to 'C'.

An example with 3 disks i.e. N=3 :
Step 1 : Shift the first disk from 'A' to 'C'.
Step 2 : Shift second disk from 'A' to 'B'.
Step 3 : Shift the first disk from 'C' to 'B'.
Step 4 : Shift the third disk from 'A' to 'C'.
Step 5 : Shift the first disk from 'B' to 'A'.
Step 6 : Shift second disk from 'B' to 'C'.
Step 7 : Shift the first disk from 'A' to 'C'

public class RecursionBasics {

    public static void towerOfHanoi(int n, String src, String helper, String dest) {
        if (n == 1) {
            System.out.println("Shift disk 1 from " + src + " to " + dest );
            return;
        }
        
        // Step 1: Move top n-1 disks from src to helper, using dest as the temporary helper
        towerOfHanoi(n - 1, src, dest, helper);
        
        // Step 2: Move the nth (largest) disk from src directly to dest
        System.out.println("Shift disk " + n + " from " + src + " to " + dest );
        
        // Step 3: Move the n-1 disks from helper to dest, using src as the temporary helper
        towerOfHanoi(n - 1, helper, src, dest);
    }

    public static void main(String args[]) {
        int n = 2; 
        System.out.println("Steps for N = " + n + ":");
        towerOfHanoi(n, "A", "B", "C");
    }
}

-----------------------------DIVIDE & CONQUER---------------------------------

// Q. --> CODE OF MERGE SORT.

public class DividenConquer{

    public static void mergeSort(int arr[],int si, int ei){
        if(si>=ei){ 
            return;
        }
        int mid= si+(ei-si)/2;
        mergeSort(arr,si,mid);
        mergeSort(arr,mid+1,ei);
        merge(arr,si,mid,ei);
    }

    public static void merge(int arr[],int si,int mid, int ei){
        int temp[]=new int[ei-si+1];
        int i=si;
        int j=mid+1;
        int k=0;

        while(i<=mid && j<=ei){
            if(arr[i]<arr[j]){
                temp[k]=arr[i];
                i++;
            }else{
                temp[k]=arr[j];
                j++;
            }
            k++;
        }

        while(i<=mid){
            temp[k++]=arr[i++];
        }
        while(j<=ei){
            temp[k++]=arr[j++];
        }
        for(k=0,i=si;k<temp.length;k++,i++){
            arr[i]=temp[k];
        }
    }
    public static void printArr(int arr[]){
        for(int i=0; i<arr.length; i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    public static void main(String args[]){
        int arr[]={6,3,9,5,2,8};
        mergeSort(arr,0,arr.length-1);
        printArr(arr);
    }
}

// Q. --> CODE OF QUICK SORT.

public class DividenConquer{

    public static void quickSort(int arr[],int si, int ei){
        if(si>=ei){
            return;
        }
        //pivot = last element 
        int pindx= Partition(arr,si,ei);
        quickSort(arr,si,pindx-1);
        quickSort(arr,pindx+1,ei);
    }
    public static int Partition(int arr[],int si,int ei){
        int pivot=arr[ei];
        int i=si-1;
        for(int j=si;j<ei; j++){
            if(arr[j]<=pivot){
                i++;
                int temp=arr[j];
                arr[j]=arr[i];
                arr[i]=temp;
            }
        }
        i++;
        int temp=pivot;
        arr[ei]=arr[i];
        arr[i]=temp;
        return i;
    }
    public static void printArr(int arr[]){
        for(int i=0; i<arr.length; i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    public static void main(String args[]){
        int arr[]={6,3,9,8,2,5};
        quickSort(arr,0,arr.length-1);
        printArr(arr);
    }
}

// Q.84 --> Search in Rotated Sorted Array                                                    { IMPORTANT FOR INTERVIEVS }
// input : sorted, rotated array with distinct numbers (in ascending order)
// It is rotated at a pivot point. Find the index of given element.

public class DividenConquer{

    public static int search(int arr[],int tar,int si,int ei){
        if(si>ei){
            return -1;
        }
        int mid=si+(ei-si)/2;
        //case Found
        if(arr[mid]==tar){
            return mid;
        }
        //tar on L1
        if(arr[si]<=arr[mid]){
            //case a: left
            if(arr[si]<=tar && tar<=arr[mid]){
                return search(arr,tar,si,mid-1);
            }else{
                //case b: right
                return search(arr,tar,mid+1,ei);
            }
        }
        //tar on L2
        else{
            //case c: right
            if(arr[mid]<=tar && tar<=arr[ei]){
                return search(arr,tar,mid+1,ei);
            }else{
                //case d: left
                return search(arr,tar,si,mid-1);
            }
        }
    }
    public static void main(String args[]){
        int arr[]={4,5,6,7,0,1,2};
        int tar=0;
        System.out.println(search(arr,tar,0,arr.length-1));
    }
}

--------------------------------------ASSIGNMENT QUESTIONS (DIVIDE & CONQUER)-------------------------------------

// Q.85 -->
// Question1:Apply Merge sort to sort an array of Strings.(Assume that all the characters in
// all the Strings are in lowercase). (EASY)
// Sample Input 1: arr = { "sun", "earth", "mars", "mercury"}
// Sample Output 1: arr = { "earth", "mars", "mercury", "sun"}

//-----------------------MY BRUTE FORCE SOLn WITH BUGS BUT WORK FOR THIS PARTICULAR QUESTION-----------------------

public class DividenConquer{

    public static void stringMergeSort(String str[],int si,int ei){
        if(si>=ei){
            return;
        }
        int mid=si+(ei-si)/2;
        stringMergeSort(str,si,mid);
        stringMergeSort(str,mid+1,ei);
        merge(str,si,mid,ei);
    }
    
    public static void merge(String str[],int si ,int mid,int ei){
        String temp[]=new String[ei-si+1];
        int i=si;
        int j=mid+1;
        int k=0;
        int l=1;

        while(i<=mid && j<=ei){
            int m=Math.min(str[i].length()-1,str[j].length()-1);
            if(str[i].charAt(0)==str[j].charAt(0)){
                    while(l<m){
                        if(str[i].charAt(l)>str[j].charAt(l)){
                            temp[k]=str[j];
                            j++;
                            break;
                        }
                        l++;
                    }
                }
            if(str[i].charAt(0)<=str[j].charAt(0)){
                temp[k]=str[i];
                i++;
            }else{
                temp[k]=str[j];
                j++;
            }
            k++;
        }
        while(i<=mid){
            temp[k++]=str[i++];
        }
        while(j<=ei){
            temp[k++]=str[j++];
        }
        for(k=0, i=si;k<temp.length;k++,i++){
            str[i]=temp[k];
        }
    }
    public static void printArr(String str[]){
        System.out.print("{ ");
        for(int i=0;i<str.length;i++){
            System.out.print(str[i]+", ");
        }
        System.out.print("}");
    }


    public static void main(String args[]){
        String str[] = { "sun", "earth", "mars", "mercury"};
        stringMergeSort(str,0,str.length-1);
        printArr(str);
    }
}

//---------------------GEMINI CORRECTED MY SOLn USING .compareTo()-----------------------

public class DividenConquer {

    // The divide stage remains perfectly correct!
    public static void stringMergeSort(String str[], int si, int ei) {
        if (si >= ei) {
            return;
        }
        int mid = si + (ei - si) / 2;
        stringMergeSort(str, si, mid);
        stringMergeSort(str, mid + 1, ei);
        merge(str, si, mid, ei);
    }
    
    // The simplified and correct merge function
    public static void merge(String str[], int si, int mid, int ei) {
        String temp[] = new String[ei - si + 1];
        int i = si;      // Pointer for left half
        int j = mid + 1; // Pointer for right half
        int k = 0;       // Pointer for temp array

        // Merge elements into temp array in sorted order
        while (i <= mid && j <= ei) {
            // compareTo returns a value < 0 if str[i] comes before str[j] alphabetically
            if (str[i].compareTo(str[j]) <= 0) {
                temp[k] = str[i];
                i++;
            } else {
                temp[k] = str[j];
                j++;
            }
            k++;
        }
        
        // Copy any remaining elements from the left subarray
        while (i <= mid) {
            temp[k++] = str[i++];
        }
        
        // Copy any remaining elements from the right subarray
        while (j <= ei) {
            temp[k++] = str[j++];
        }
        
        // Transfer elements from temp back to the original array
        for (k = 0, i = si; k < temp.length; k++, i++) {
            str[i] = temp[k];
        }
    }

    public static void printArr(String str[]) {
        System.out.print("{ ");
        for (int i = 0; i < str.length; i++) {
            System.out.print("\"" + str[i] + "\"" + (i < str.length - 1 ? ", " : ""));
        }
        System.out.println(" }");
    }

    public static void main(String args[]) {
        String str[] = { "sun", "earth", "mars", "mercury" };
        stringMergeSort(str, 0, str.length - 1);
        printArr(str);
    }
}
-------------------------OR--------------------------------

public class DividenConquer {

    //function to mergeSort 2 arrays
    public static String[] mergeSort(String[] arr, int lo, int hi) {
        if (lo == hi) {
            String[] A = { arr[lo] };
            return A;
        }

        int mid = lo + (hi-lo) / 2;
        String[] arr1 = mergeSort(arr, lo, mid);
        String[] arr2 = mergeSort(arr, mid + 1, hi);
        String[] arr3 = merge(arr1, arr2);
        return arr3;
    }
    static String[] merge(String[] arr1, String[] arr2) {
        int m = arr1.length;
        int n = arr2.length;
        String[] arr3 = new String[m + n];
        int idx = 0;
        int i = 0;
        int j = 0;
        while (i < m && j < n) {
            if (isAlphabeticallySmaller(arr1[i], arr2[j])) {
                arr3[idx] = arr1[i];
                i++;
                idx++;
            }
            else {
                arr3[idx] = arr2[j];
                j++;
                idx++;
            }
        }
        while (i < m) {
            arr3[idx] = arr1[i];
            i++;
            idx++;
        }
        while (j < n) {
            arr3[idx] = arr2[j];
            j++;
            idx++;
        }
        return arr3;
    }
    // Return true if str1 appears before str2 in alphabetical order
    static boolean isAlphabeticallySmaller(String str1, String str2) {
        if (str1.compareTo(str2) < 0) {
            return true;
        }
        return false;
    }
    public static void main(String[] args) {
        String[] arr = { "sun", "earth", "mars", "mercury" };
        String[] a = mergeSort(arr, 0, arr.length-1);
        for (int i = 0; i < a.length; i++) {
            System.out.println(a[i]);
        }
    }
}

// Q.86 -->
// Question 2 : Given an array nums of size n, return the majority element. (MEDIUM)
// The majority element is the element that appears more than ⌊n/2⌋ times.You may assume
// that the majority element always exists in the array.
// Sample Input 1: nums = [3,2,3]
// Sample Output 1: 3
// Sample Input 2: nums = [2,2,1,1,1,2,2]
// Sample Output 2: 2
// Constraints(extra Conditions):
// ● n == nums.length
// ● 1 <= n <= 5 * 104
// ●-109 <= nums[i] <= 109

//---------------------MY BRUTE FORCE SOLn -> (n2)-----------------------

public class DividenConquer{

    public static int majorityElt(int nums[]){
        int majorityCount = nums.length/2;
        for(int i=0;i<nums.length;i++){
            int count=0;
            for(int j=0;j<nums.length;j++){
                if(nums[i]==nums[j]){
                    count++;
                }
            }
            if(count > majorityCount){
                return nums[i];
            }
        }
        return -1;
    }
    public static void main(String args[]){
        int nums[] = {3,2,3};   
        for(int i=0;i<nums.length;i++){
            System.out.print(nums[i]+" ");
        }System.out.println();
        System.out.println(majorityElt(nums));
    }
}

//-----------------------USING (DIVIDE & CONQUER) -> (nlogn)-------------------

public class DividenConquer {

    // Helper method to count occurrences of a target number in a specific range
    private static int countInRange(int[] nums, int num, int lo, int hi) {
        int count = 0;
        for (int i = lo; i <= hi; i++) {
            if (nums[i] == num) {
                count++;
            }
        }
        return count;
    }

    private static int majorityEltRec(int[] nums, int lo, int hi) {
        // Base case: single element array range
        if (lo == hi) {
            return nums[lo];
        }

        // Divide
        int mid = lo + (hi - lo) / 2;
        
        // Conquer
        int leftMajority = majorityEltRec(nums, lo, mid);
        int rightMajority = majorityEltRec(nums, mid + 1, hi);

        // Combine
        if (leftMajority == rightMajority) {
            return leftMajority;
        }

        // If they disagree, count both candidates in the full current range
        int leftCount = countInRange(nums, leftMajority, lo, hi);
        int rightCount = countInRange(nums, rightMajority, lo, hi);

        return leftCount > rightCount ? leftMajority : rightMajority;
    }

    public static int majorityElt(int[] nums) {
        return majorityEltRec(nums, 0, nums.length - 1);
    }

    public static void main(String args[]) {
        int nums[] = {3, 2, 3};   
        System.out.println("Majority Element (Divide & Conquer): " + majorityElt(nums));
    }
}

// Q.87 -->
// Question 3 : Given an array of integers. Find the Inversion Count in the array. (HARD)

// Inversion Count:Foranarray, inversion count indicate show far(or close)the array is from
// being  sorted. If thearray is already sorted then the inversion count is 0. If an array is
// sorted in the reverse order then the inversion count is the maximum.
// Formally, two elements a[i] and a[j] form an inversion if a[i] > a[j] and i < j.

// Sample Input 1: N = 5, arr[ ] = {2, 4, 1, 3, 5}
// Sample Output 1: 3, because it has 3 inversions -(2, 1), (4, 1), (4, 3).

// Sample Input 2 : N = 5, arr[ ] = {2, 3, 4, 5, 6}
// Sample Output 2 : 0, because the array is already sorted

// Sample Input 3 : N = 3, arr[] = {5, 5, 5}
// Sample Output 3 : 0, because all the elements of the array are the same & already in a sorted
// manner.

// (Hint : A sorting algorithm will be used to solve this question.)
// Note- This question is important. Even if you are not able to come up with the approach,
// please understand the solution.


//-----------MY BRUTE FORCE SOLn -> (n2)-----------

public class DividenConquer{

    public static int countInversion(int arr[]){
        int count =0;
        for(int i =0; i<arr.length; i++){
            for(int j=i+1; j<arr.length; j++){
                if(arr[j]<arr[i]){
                    count++;
                }
            }
        }
        return count;
    }
    public static void main(String args[]){
        int arr[] = {5, 5, 5};
        System.out.println("Inversion count is: "+countInversion(arr));
    }
}

//-----------GEMINI CORRECTED MY SOLn WITH count += (mid - i + 1), BUT IT IS NOT BEST SOLn BECAUSE HERE STATIC VARIABLE IS USED-------------

public class DividenConquer {

    static int count = 0;
    //Using a static global variable for tracking state is generally considered poor programming practice because:
    It isn't reusable: If you call countInversion() a second time in your main method on a different array, it won't start from 0; it will keep adding to the previous total unless you manually reset it.
    It isn't thread-safe: If multiple parts of a program try to count inversions at the same time, they will corrupt each other's counts.

    public static void countInversion(int arr[], int si, int ei) {
        if (si >= ei) {
            return;
        }
        int mid = si + (ei - si) / 2;
        countInversion(arr, si, mid);
        countInversion(arr, mid + 1, ei);
        merge(arr, si, mid, ei);
    }

    public static void merge(int arr[], int si, int mid, int ei) {
        int temp[] = new int[ei - si + 1];
        int i = si;
        int j = mid + 1;
        int k = 0;

        while (i <= mid && j <= ei) {
            if (arr[i] <= arr[j]) {
                temp[k] = arr[i];
                i++;
            } else {
                temp[k] = arr[j];
                j++;
                // All remaining elements in left subarray are inversions
                count += (mid - i + 1); 
            }
            k++;
        }

        while (i <= mid) {
            temp[k++] = arr[i++];
        }
        while (j <= ei) {
            temp[k++] = arr[j++];
        }
        for (k = 0, i = si; k < temp.length; k++, i++) {
            arr[i] = temp[k];
        }
    }

    public static void main(String args[]) {
        int arr[] = {2, 4, 1, 3, 5};
        countInversion(arr, 0, arr.length - 1);
        System.out.println("Inversion count is: " + count); 
    }
}

-------------------------BEST SOLn--------------------------------

public class DividenConquer {

    // 1. Clean, safe entry point that returns the value directly
    public static int getInversions(int arr[]) {
        return mergeSortAndCount(arr, 0, arr.length - 1);
    }

    // 2. Pure recursive function (No global variables)
    private static int mergeSortAndCount(int arr[], int si, int ei) {
        int count = 0;
        if (si < ei) {
            int mid = si + (ei - si) / 2;

            count += mergeSortAndCount(arr, si, mid);
            count += mergeSortAndCount(arr, mid + 1, ei);
            count += mergeAndCount(arr, si, mid, ei);
        }
        return count;
    }

    // 3. Clean, readable standard merge logic
    private static int mergeAndCount(int arr[], int si, int mid, int ei) {
        int temp[] = new int[ei - si + 1];
        int i = si;
        int j = mid + 1;
        int k = 0;
        int count = 0;

        while (i <= mid && j <= ei) {
            if (arr[i] <= arr[j]) {
                temp[k++] = arr[i++];
            } else {
                temp[k++] = arr[j++];
                count += (mid - i + 1); // Clean standard formula
            }
        }

        while (i <= mid) {
            temp[k++] = arr[i++];
        }
        while (j <= ei) {
            temp[k++] = arr[j++];
        }

        for (k = 0, i = si; k < temp.length; k++, i++) {
            arr[i] = temp[k];
        }
        return count;
    }

    public static void main(String args[]) {
        int arr[] = {2, 4, 1, 3, 5};
        System.out.println("Inversion count is: " + getInversions(arr)); // Output: 3
    }
}


    
------------------------------------------------BACKTRACKING----------------------------------------------------

// Q. --> BACKTRACKING ARRAYS -- ONLY FOR UNDERSTANDING.

public class Backtracking {

    public static void changeArr(int arr[], int i, int val){
        if(i==arr.length){
            printArr(arr);
            return;
        }
        arr[i]=val;
        changeArr(arr,i+1,val+1);
        arr[i]=arr[i]-2;
    }

    public static void printArr(int arr[]){
        for(int i=0; i<arr.length; i++){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
    }
    
    public static void main(String args[]){
        int arr[]=new int[5];
        changeArr(arr,0,1);
        printArr(arr);
    }
}

// Q.88 --> FIND & PRINT ALL SUBSETS OF A GIVEN STRING.

public class Backtracking {

    public static void findSubsets(String str,String ans,int i){
        if(i==str.length()){
            if(ans.length()==0){
                System.out.println("null");
            }else{
                System.out.println(ans);
            }
            return;
        }
        //Yes choice
        findSubsets(str,ans+str.charAt(i),i+1);
        //No choice
        findSubsets(str,ans,i+1);
    }

    public static void main(String args[]){
        String str="abc";
        findSubsets(str,"",0);
    }
}

// Q.89 --> FIND & PRINT ALL PERMUTATIONS OF A STRING.

public class Backtracking {

    public static void findPermutations(String str, String ans){
        if(str.length()==0){
            System.out.println(ans);
            return;
        }
        //recursion
        for(int i=0; i<str.length(); i++){
            char curr = str.charAt(i);
            String newStr = str.substring(0,i) + str.substring(i+1);
            findPermutations(newStr,ans+curr);
        }
    }

    public static void main(String args[]){
        String str="abc";
        findPermutations(str,"");
    }
}

// Q.90 --> N-QUEENS PROBLEM { FIND & PRINT ALL POSSIBLE SOLn }.

public class Backtracking {

    public static boolean isSafe(char board[][],int row, int col){
        //verticle up
        for(int i=row-1; i>=0; i--){
            if(board[i][col]=='Q'){
                return false;
            }
        }
        //diag left up
        for(int i=row-1, j=col-1; i>=0 && j>=0; i--,j--){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        //diag right up
        for(int i=row-1, j=col+1; i>=0 && j<board.length; i--,j++){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        return true;
    }

    public static void nQueens(char board[][],int row){
        if(row==board.length){
            printBoard(board);
            return;
        }
        for(int j=0; j<board.length; j++){
            if(isSafe(board,row,j)){
                board[row][j]='Q';
                nQueens(board,row+1);//fxn call
                board[row][j]='x';//backtracking step
            }
        }
    }

    public static void printBoard(char board[][]){
        System.out.println("----------------chess board----------------");
        for(int i=0; i<board.length; i++){
            for(int j=0; j<board.length; j++){
                System.out.print(board[i][j]+" ");
            }System.out.println();
        }
    }
    
    public static void main(String args[]){
        int n=4;
        char board[][]=new char[n][n];
        for(int i=0; i<n; i++){
            for(int j=0; j<n; j++){
                board[i][j]='x';
            }
        }
        nQueens(board,0);
    }
}

// Q.91 --> N-QUEENS PROBLEM { COUNT TOTAL WAYS TO SOLVE }.

public class Backtracking {

    public static boolean isSafe(char board[][],int row, int col){
        //verticle up
        for(int i=row-1; i>=0; i--){
            if(board[i][col]=='Q'){
                return false;
            }
        }
        //diag left up
        for(int i=row-1, j=col-1; i>=0 && j>=0; i--,j--){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        //diag right up
        for(int i=row-1, j=col+1; i>=0 && j<board.length; i--,j++){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        return true;
    }

    static int count=0;
    public static void nQueens(char board[][],int row){
        if(row==board.length){
            //printBoard(board);
            count++;
            return;
        }
        for(int j=0; j<board.length; j++){
            if(isSafe(board,row,j)){
                board[row][j]='Q';
                nQueens(board,row+1);//fxn call
                board[row][j]='x';//backtracking step
            }
        }
    }

    public static void main(String args[]){
        int n=4;
        char board[][]=new char[n][n];
        nQueens(board,0);
        System.out.println("Total ways to solve the N-Queens problem is: "+count);
    }
}

// Q.92 --> N-QUEENS PROBLEM { CHECK IF PROBLEM CAN BE SOLVED & PRINT ONLY ONE SOLn }

public class Backtracking {

    public static boolean isSafe(char board[][],int row, int col){
        //verticle up
        for(int i=row-1; i>=0; i--){
            if(board[i][col]=='Q'){
                return false;
            }
        }
        //diag left up
        for(int i=row-1, j=col-1; i>=0 && j>=0; i--,j--){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        //diag right up
        for(int i=row-1, j=col+1; i>=0 && j<board.length; i--,j++){
            if(board[i][j]=='Q'){
                return false;
            }
        }
        return true;
    }

    public static boolean nQueens(char board[][],int row){
        if(row==board.length){
            return true;
        }
        for(int j=0; j<board.length; j++){
            if(isSafe(board,row,j)){
                board[row][j]='Q';
                if(nQueens(board,row+1)){//fxn call
                    return true;
                }
                board[row][j]='x';//backtracking step
            }
        }

        return false;
    }

    public static void printBoard(char board[][]){
        System.out.println("----------------chess board----------------");
        for(int i=0; i<board.length; i++){
            for(int j=0; j<board.length; j++){
                System.out.print(board[i][j]+" ");
            }System.out.println();
        }
    }

    public static void main(String args[]){
        int n=4;
        char board[][]=new char[n][n];
        for(int i=0; i<n; i++){
            for(int j=0; j<n; j++){
                board[i][j]='x';
            }
        }
        if(nQueens(board,0)){
            System.out.println("Yes, Problem can be solved.");
            printBoard(board);
        }else{
            System.out.println("No, Problem can not be solved.");
        }
    }
}

// Q.93 --> FIND NUMBER OF WAYS TO REACH FROM (0,0) TO (N-1,M-1) IN A NxM GRID.
            ALLOWS MOVES --> RIGHT OR DOWN.

public class Backtracking{

    public static int gridWays(int grid[][],int d,int r){
        int n=grid.length;//rows
        int m=grid[0].length;//columns

        if(d==n-1 && r==m-1){
            return 1;
        }else if(d==n || r==m){
            return 0;
        }

        return gridWays(grid,d+1,r) + gridWays(grid,d,r+1);
    }
    public static void main(String args[]){
        int n=3,m=2;
        int grid[][]=new int[n][m];
        System.out.println(gridWays(grid,0,0));
    }
}

-------------OR-------------

public class Backtracking{

    public static int gridWays(int n,int m,int d,int r){
        if(d==n-1 && r==m-1){
            return 1;
        }else if(d==n || r==m){
            return 0;
        }
        int w1 = gridWays(n,m,d+1,r);
        int w2 = gridWays(n,m,d,r+1);
        return w1 + w2;
    }
    public static void main(String args[]){
        int n=3,m=2;
        System.out.println(gridWays(n,m,0,0));
    }
}

-------------OPTIMIZED O(N+M)--------------

public class Backtracking{

    //USING MATH TRICK --> PERMUTATION
    public static int gridWays(int n,int m,int d,int r){
        if(d==n-1 && r==m-1){
            return 1;
        }else if(d==n || r==m){
            return 0;
        }
        int w1 = gridWays(n,m,d+1,r);
        int w2 = gridWays(n,m,d,r+1);
        return w1 + w2;
    }
    public static void main(String args[]){
        int n=3,m=2;
        System.out.println(gridWays(n,m,0,0));
    }
}

// Q.94 --> WRITE A FUNCTION TO COMPLESTE A SUDOKU.

public class Backtracking{

    public static boolean isSafe(int sudoku[][],int digit, int row, int col){
        //row & col
        for(int i=0; i<=8; i++){
            if(sudoku[row][i]==digit || sudoku[i][col]==digit){
                return false;
            }
        }
        //grid
        int sr = (row/3)*3;
        int sc = (col/3)*3;
        for(int i=sr; i<sr+3; i++){
            for(int j=sc; j<sc+3; j++){
               if(sudoku[i][j]==digit){
                return false;
               }
            }
        }
        return true;
    }

    public static boolean sudokuSolver(int sudoku[][],int row, int col){
        if(row == 9){
            return true;
        }

        int nextRow = row;
        int nextCol = col+1;
        if(col+1 == 9){
            nextRow = row+1;
            nextCol = 0;
        }

        if(sudoku[row][col] != 0){
            return sudokuSolver(sudoku,nextRow,nextCol);
        }
        for(int digit=1; digit<=9; digit++){
            if(isSafe(sudoku,digit,row,col)){
                sudoku[row][col]=digit;
                if(sudokuSolver(sudoku,nextRow,nextCol)){
                    return true;
                }
                sudoku[row][col]=0;
            }
        }
        return false;
    }

    public static void printSudoku(int sudoku[][]){
        for(int i=0; i<9; i++){
            for(int j=0; j<9; j++){
               System.out.print(sudoku[i][j]+" ");
            }System.out.println();
        }
    }
    public static void main(String args[]){

        int sudoku[][] = {  {0, 0, 8, 0, 0, 0, 0, 0, 0},
                            {4, 9, 0, 1, 5, 7, 0, 0, 2},
                            {0, 0, 3, 0, 0, 4, 1, 9, 0},
                            {1, 8, 5, 0, 6, 0, 0, 2, 0},
                            {0, 0, 0, 0, 2, 0, 0, 6, 0},
                            {9, 6, 0, 4, 0, 5, 3, 0, 0},
                            {0, 3, 0, 0, 7, 2, 0, 0, 4},
                            {0, 4, 9, 0, 3, 0, 0, 5, 7},
                            {8, 2, 7, 0, 0, 9, 0, 1, 3} 
                        };
        if(sudokuSolver(sudoku,0,0)){
            System.out.println("Soln exists.");
            printSudoku(sudoku);
        }else{
            System.out.println("Soln does not exist.");
        }
    }
}

-------------------------------ASSIGNMENT QUESTION {BACKTRACKING}-----------------------------------
// Q.95 -->
Question 1 :
Rat in a Maze
You are given a starting position for a rat which is stuck in a maze at an initial point (0, 0) (the
maze can be thought of as a 2-dimensional plane). The maze would be given in the form of a
square matrix of order N * N where the cells with value 0 represent the maze’s blocked
locations while value 1 is the open/available path that the rat can take to reach its destination.
The rat's destination is at (N - 1, N - 1).
Your task is to find all the possible paths that the rat can take to reach from source to
destination in the maze.
The possible directions that it can take to move in the maze are 'U'(up) i.e. (x, y- 1) , 'D'(down)
i.e. (x, y + 1) , 'L' (left) i.e. (x - 1, y), 'R' (right) i.e. (x + 1, y).
(This problem is similar to Grid ways.)
<img width="767" height="436" alt="image" src="https://github.com/user-attachments/assets/dba8eb2d-5938-4855-a941-88491ec77bb7" />

Sample Input : int maze[][] = 
{ { 1, 0, 0, 0 },
{ 1, 1, 0, 1 },
{ 0, 1, 0, 0 },
{ 1, 1, 1, 1 } };

Sample Output : 
1  0  0  0
1  1  0  0
0  1  0  0
0  1  1  1

public class Backtracking {

    public static boolean isSafe(int maze[][],int x, int y, int sol[][]){
        return ( x>=0 && x<maze.length &&
                 y>=0 && y<maze[0].length 
                 && maze[x][y]==1 && sol[x][y]==0  );
    }

    public static void solveMaze(int maze[][],int x, int y){
        int n=maze.length;
        int m=maze[0].length;

        int sol[][]=new int [n][m];
        solveMazeUtil(maze,x,y,sol);
    }

    public static boolean solveMazeUtil(int maze[][],int x, int y,int sol[][]){
        if(x==maze.length-1 && y==maze[0].length-1 && maze[x][y]==1 ){
            sol[x][y]=1;
            printMaze(sol);
            sol[x][y]=0;
            return true;
        }
        if(isSafe(maze,x,y,sol)){
            sol[x][y]=1;
            if(solveMazeUtil(maze,x+1,y,sol)){   //down
                return true;    
            }
            if(solveMazeUtil(maze,x,y+1,sol)){   //rigth
                return true;
            }
            if(solveMazeUtil(maze,x,y-1,sol)){   //left
                return true;
            }
            if(solveMazeUtil(maze,x-1,y,sol)){   //up
                return true;
            }
            sol[x][y]=0;     //backtracking step
        }
        return false;
    }

    public static void printMaze(int maze[][]){
        for(int i=0; i<maze.length; i++){
            for(int j=0; j<maze[0].length; j++){
                System.out.print(maze[i][j]+" ");
            }System.out.println();
        }System.out.println();
    }

    public static void main(String args[]) {
        int maze[][] = {  
            { 1, 1, 1, 1 },
            { 1, 1, 0, 1 },
            { 1, 1, 1, 1 },
            { 1, 1, 1, 1 } 
        };
        
        solveMaze(maze, 0, 0);
    }
}
----------------TO PRINT ALL POSSIBLE SOLn-----------------

public class Backtracking {

    public static boolean isSafe(int maze[][], int x, int y, int sol[][]) {
        return (x >= 0 && x < maze.length && 
                y >= 0 && y < maze[0].length && 
                maze[x][y] == 1 && sol[x][y] == 0);
    }

    public static void solveMaze(int maze[][], int x, int y) {
        int rows = maze.length;
        int cols = maze[0].length;
        int sol[][] = new int[rows][cols]; 
        
        System.out.println("--- Finding All Solutions ---");
        solveMazeUtil(maze, x, y, sol);
    }

    public static void solveMazeUtil(int maze[][], int x, int y, int sol[][]) {
        // Base Case: Reached the end
        if (x == maze.length - 1 && y == maze[0].length - 1 && maze[x][y] == 1) {
            sol[x][y] = 1;
            System.out.println("Solution Found:");
            printMaze(sol);
            System.out.println();
            sol[x][y] = 0; // Backtrack the final step
            return;
        }

        if (isSafe(maze, x, y, sol)) {
            sol[x][y] = 1; // Mark current cell in path

            solveMazeUtil(maze, x + 1, y, sol); // Down
            solveMazeUtil(maze, x, y + 1, sol); // Right
            solveMazeUtil(maze, x, y - 1, sol); // Left
            solveMazeUtil(maze, x - 1, y, sol); // Up

            sol[x][y] = 0; // Backtrack completely to try new paths
        }
    }

    public static void printMaze(int maze[][]) {
        for (int i = 0; i < maze.length; i++) {
            for (int j = 0; j < maze[0].length; j++) {
                System.out.print(maze[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void main(String args[]) {
        int maze[][] = {  
            { 1, 1, 1, 1 },
            { 0, 1, 0, 1 },
            { 1, 1, 1, 1 },
            { 1, 0, 1, 1 } 
        };
        
        solveMaze(maze, 0, 0);
    }
}
    
<img width="566" height="667" alt="image" src="https://github.com/user-attachments/assets/73a40c1a-1fed-4dd8-8ce0-5ceba948ec3c" /> <img width="1321" height="670" alt="image" src="https://github.com/user-attachments/assets/d9c28c92-0dd5-4dd8-984e-e2c6393cabe2" />

// Q.96 -->
Question 2 :
**Keypad Combinations**
Given a string containing digits from 2-9 inclusive, print all possible letter combinations that
the number could represent. You can print the answer in any order.
A mapping of digits to letters (just like on the telephone buttons) is given below.Note that 1
does not map to any letters.

<img width="400" height="270" alt="image" src="https://github.com/user-attachments/assets/4d0cc85f-69dc-41ce-999d-5c4c0fd33a6a" />

Sample Input 1: digits = "23"
Sample Output 1: "ad", "ae", "af", "bd", "be", "bf", "cd", "ce", "cf"

Sample Input 2: digits = "2"
Sample Output 2: "a", "b", "c"

Sample Input 3: digits = ""
Sample Output 3: ””

------------------------------MY SOLn IMPROVED BY GEMENI-----------------------------
public class Backtracking{

    static String str[]={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
    public static void keypadStringCombinations(String digits,String ans,int i){
        if(i==digits.length()){
            if(ans.isEmpty()){
                System.out.println("\nnull");
            }else{
                System.out.print(ans+" ");
            }
            return;
        }
        //digits.charAt(i) gives character like '2','3' but not any integer
        int digitIndex = helper(digits.charAt(i));
        if(digitIndex ==-1){
            keypadStringCombinations(digits,ans,i+1);
            return;
        }
        String curr =str[digitIndex];
        for(int j=0; j<curr.length(); j++){
            Character ch=curr.charAt(j);
            keypadStringCombinations(digits,ans+ch,i+1);
        }
    }

    public static int helper(Character ch){
        switch(ch){
            case '2':return 2;
            case '3':return 3;
            case '4':return 4;
            case '5':return 5;
            case '6':return 6;
            case '7':return 7;
            case '8':return 8;
            case '9':return 9;
            default:return -1;
        }
    }
    public static void main(String args[]){
        keypadStringCombinations("23","",0);
    }
}
-----------------OR-------------------

public class Backtracking{

    static String str[]={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
    public static void keypadStringCombinations(String digits,String ans,int i){
        if(i==digits.length()){
            if(ans.isEmpty()){
                System.out.println("\nnull");
            }else{
                System.out.print(ans+" ");
            }
            return;
        }
        // Convert char to int directly (e.g., '2' - '0' = 2)
        int digitIndex = digits.charAt(i) - '0';
        if(digitIndex < 2 || digitIndex > 9){
            keypadStringCombinations(digits,ans,i+1);
            return;
        }
        String curr =str[digitIndex];
        for(int j=0; j<curr.length(); j++){
            Character ch=curr.charAt(j);
            keypadStringCombinations(digits,ans+ch,i+1);
        }
    }

    public static void main(String args[]){
        keypadStringCombinations("23","",0);
    }
}

--------------STRUCTURED & GOOD SOLN------------------

public class Backtracking {

    final static char[][] L = { {},{},{'a','b','c'},{'d','e','f'},{'g','h','i'},
                                {'j','k','l'},{'m','n','o'},{'p','q','r','s'},
                                {'t','u','v'},{'w','x','y','z'}
                              };

    public static void letterCombinations(String D) {
        if (D == null || D.isEmpty()) {
            System.out.println("null");
            return;
        }
        // Pass a single StringBuilder instance down the stack
        dfs(0, new StringBuilder(), D);
    }

    public static void dfs(int pos, StringBuilder sb, String D) {
        if (pos == D.length()) {
            System.out.print(sb.toString() + " ");
            return;
        }

        int digit = Character.getNumericValue(D.charAt(pos));
        // Safety check for 0, 1, or non-digits
        if (digit < 2 || digit > 9) {
            dfs(pos + 1, sb, D);
            return;
        }

        char[] letters = L[digit];
        for (int i = 0; i < letters.length; i++) {
            sb.append(letters[i]);       // 1. Choose: Add the letter
            dfs(pos + 1, sb, D);         // 2. Explore: Go deeper
            sb.deleteCharAt(sb.length() - 1); // 3. Un-choose: Backtrack (remove the letter)
        }
    }

    public static void main(String args[]) {
        letterCombinations("23");
    }
}

// Q.97 -->
Question 3 :
Knight’s Tour
Given a N*N board with the Knight placed on the first block of an empty board. Moving
according to the rules of chess, knights must visit each square exactly once. Print the order of
each cell in which they are visited.

Sample Input 1 : N = 8
Sample Output 1 :
0  59  38  33  30  17   8  63
37  34  31  60   9  62  29  16
58   1  36  39  32  27  18   7
35  48  41  26  61  10  15  28
42  57   2  49  40  23   6  19
47  50  45  54  25  20  11  14
56  43  52   3  22  13  24   5
51  46  55  44  53   4  21  12

(Hint : Similar to N Queens

//CONTINUING THE DSA AFTER 18 DAYS BCZ OF SOME REASONS AND SOMETIME NOT WILLING TO START, PLAYING GAMES BGMI, POKEMON AND WATCHED MOVIES.
public class Backtracking {

    public static boolean isSafe(int board[][],int row, int col){
        return (row>=0 && row<board.length && 
                col>=0 && col<board[0].length && 
                board[row][col]==0);
    } 
    public static boolean nKnight(int board[][],int row,int col,int moveNum){
        if(moveNum==board.length*board[0].length){
            board[row][col]=moveNum;
            printBoard(board);
            return true;
        }
        board[row][col]=moveNum;
        // upto N=6 U can make array of xMove & yMove in any order like commented array
        //but Backtrecking uses the DFS so according to that non commented array
        //is Good and take less time
        // int xMove[]={2,2,1,1,-2,-2,-1,-1};
        // int yMove[]={1,-1,2,-2,1,-1,2,-2};
        int xMove[] = { 2, 1, -1, -2, -2, -1,  1,  2 };
        int yMove[] = { 1, 2,  2,  1, -1, -2, -2, -1 };
        for(int i=0; i<8; i++){
            int nextRow=row +xMove[i];
            int nextCol=col +yMove[i];
            if(isSafe(board,nextRow,nextCol)){
                if(nKnight(board,nextRow,nextCol,moveNum+1)){
                    return true;
                }
            }
        }
        board[row][col]=0;
        return false;
    }

    public static void printBoard(int board[][]){
        for(int i=0; i<board.length; i++){
            for(int j=0; j<board[0].length; j++){
                System.out.printf("%2d ", board[i][j]);
            }System.out.println();
        }System.out.println();
    }
    public static void main(String args[]) {
        int N=8;
        int board[][]=new int[N][N];
        nKnight(board,0,0,1);
    }
}

------------------------------------------------ARRAYLIST (VECTOR)----------------------------------------------------

// Q. --> OPERATION IN ARAYLIST.

import java.util.ArrayList;
public class ClassRoom {

    public static void main(String args[]){
        ArrayList<Integer> list=new ArrayList<>();
        //add elt in ArrayList --> add operation
        list.add(2);
        list.add(5);
        list.add(9);
        list.add(3);
        list.add(6);

        //print list
        System.out.println(list);

        //get elt from list --> get operation
        System.out.println(list.get(2));

        //remove elt from list --> remove operation
        list.remove(2);
        System.out.println(list);

        //set (repalace) elt in list --> set operation
        list.set(2,10);
        System.out.println(list);

        //check elt in list --> contain operation
        System.out.println(list.contains(11));

        //add elt at an index --> add operation
        list.add(2,3);
        System.out.println(list);

        //size of Arraylist
        System.out.println(list.size());

        //print all elt of ArrayList like Array
        for(int i=0; i<list.size(); i++){
            System.out.print(list.get(i)+" ");
        }System.out.println();

        //Print in reverse order
        for(int i=list.size()-1; i>=0; i--){
            System.out.print(list.get(i)+" ");
        }System.out.println();

        //Find max in ArrayList
        int maxVal=Integer.MIN_VALUE;
        for(int i=0; i<list.size(); i++){
            maxVal=Math.max(maxVal,list.get(i));
        }System.out.println(maxVal);
        
        //swap elt in ArrayList
        int idx1=1,idx2=3;
        int temp=list.get(idx1);
        list.set(idx1,list.get(idx2));
        list.set(idx2,temp);
        
        System.out.println(list);
    }
    
}

// Q. --> WRITE A FUNCTION TO SWAP ELT IN ARRAYLIST.

import java.util.ArrayList;
public class ClassRoom {

    public static void swap(ArrayList<Integer> list,int idx1, int idx2){
        int temp=list.get(idx1);
        list.set(idx1,list.get(idx2));
        list.set(idx2,temp);
    }
    public static void main(String args[]){
    
        ArrayList<Integer> list=new ArrayList<>();
        list.add(2);
        list.add(5);
        list.add(9);
        list.add(3);
        list.add(6);
        System.out.println(list);
        swap(list,1,3);
        System.out.println(list);
    }
    
}

// Q. --> SORT AN ARRYAYLIST ( BOTH IN ASCENDING AND DESCENDING ).

import java.util.ArrayList;
import java.util.Collections;
//or in place of both above U can use import java.util.*;
public class ClassRoom {

    public static void main(String args[]){
        ArrayList<Integer> list=new ArrayList<>();
        list.add(2);
        list.add(5);
        list.add(9);
        list.add(3);
        list.add(6);

        System.out.println(list);

        //sorting ArrayList 
        Collections.sort(list);
        System.out.println(list);
        
        //sorting in reverse order
        Collections.sort(list, Collections.reverseOrder());
        System.out.println(list);

    }
    
}

// Q.98 --> FOR GIVEN N LINES ON X-AXIS, USE 2 LINES TO FORM A CONTAINER SUCH THAT IT HOLDS MAXIMUM WATER.            { AKSED IN -- FLIPKART, DUNZO }    
 height = {1,8,6,2,5,4,8,3,7}
 <img width="842" height="502" alt="image" src="https://github.com/user-attachments/assets/2e7e6829-2356-4f05-9b84-248b9d6eda28" />

 import java.util.ArrayList;
public class ClassRoom{

    public static int maxWater(ArrayList<Integer> height){
        int area=0;
        for(int i=0; i<height.size(); i++){
            for(int j=i+1; j<height.size(); j++){
                area=Math.max(area,(Math.min(height.get(i),height.get(j))*(j-i)));
            }
        }
        return area;
    }
    public static void main(String args[]){
        ArrayList<Integer> height =new ArrayList<>();
        //1 8 6 2 5 4 8 3 7
        height.add(1);
        height.add(8);
        height.add(6);
        height.add(2);
        height.add(5);
        height.add(4);
        height.add(8);
        height.add(3);
        height.add(7);
        System.out.println(height);
        System.out.println(maxWater(height));
    }
}

----------------------2 POINTER APPROACH --> O(n)-------------------------

import java.util.ArrayList;
public class ClassRoom{

    //2 pointer approach --> O(n)
    public static int maxWater(ArrayList<Integer> height){
        int maxWater=0;
        int lp=0;
        int rp=height.size()-1;
        while(lp < rp){
            //Calculate Area
            int ht=Math.min(height.get(lp),height.get(rp));
            int width= rp-lp;
            maxWater =Math.max(maxWater,ht*width);
            //update ptr
            if(height.get(lp) < height.get(rp)){
                lp++;
            }else{
                rp--;
            }
        }
        return maxWater;
    }
    public static void main(String args[]){
        ArrayList<Integer> height =new ArrayList<>();
        //1 8 6 2 5 4 8 3 7
        height.add(1);
        height.add(8);
        height.add(6);
        height.add(2);
        height.add(5);
        height.add(4);
        height.add(8);
        height.add(3);
        height.add(7);
        System.out.println(height);
        System.out.println(maxWater(height));
    }
}

// Q.99 --> PAIR SUM 1

FIND IF ANY PAIR IN A SORTED ARRAYLIST HAS A TARGET SUM.
list={1,2,3,4,5}, target=5

import java.util.ArrayList;
public class ClassRoom{

    //BruteForce
    public static boolean pairSum1(ArrayList<Integer> list, int target){
        for(int i=0; i<list.size(); i++){
            for(int j=i+1; j<list.size(); j++){
                if(list.get(i)+list.get(j)==target){
                    return true;
                }
            }
        }
        return false;
    }
    public static void main(String args[]){
        ArrayList<Integer> list= new ArrayList<>();
        for(int i=1; i<=5; i++){
            list.add(i);
        } 
        System.out.println(list);
        System.out.println(pairSum1(list,5));
    }
}

----------------------2 POINTER APPROACH --> O(n)-------------------------

import java.util.ArrayList;
public class ClassRoom{

    public static boolean pairSum1(ArrayList<Integer> list, int target){
        int lp=0;
        int rp=list.size()-1;
        while(lp < rp){
            if(list.get(lp)+list.get(rp) ==target){
                return true;
            }else if(list.get(lp)+list.get(rp) >target){
                rp--;
            }else{
                lp++;
            }
        }
        return false;
    }
    public static void main(String args[]){
        ArrayList<Integer> list= new ArrayList<>();
        for(int i=1; i<=5; i++){
            list.add(i);
        } 
        System.out.println(list);
        System.out.println(pairSum1(list,5));
    }
}

// Q.100 --> PAIR SUM 2

FIND IF ANY PAIR IN A SORTED & ROTATED ARRAYLIST HAS A TARGET SUM.
list={11,15,6,8,9,10}, target=16

import java.util.ArrayList;
public class ClassRoom{

    //BruteForce
    public static boolean pairSum1(ArrayList<Integer> list, int target){
        for(int i=0; i<list.size(); i++){
            for(int j=i+1; j<list.size(); j++){
                if(list.get(i)+list.get(j)==target){
                    return true;
                }
            }
        }
        return false;
    }
    public static void main(String args[]){
        ArrayList<Integer> list= new ArrayList<>();
        for(int i=1; i<=5; i++){
            list.add(i);
        } 
        System.out.println(list);
        System.out.println(pairSum1(list,5));
    }
}

----------------------2 POINTER APPROACH WITH MODULO ARITHMETIC --> O(n)-------------------------                                { IMP, MUST REMEMBER THIS }

import java.util.ArrayList;
public class ClassRoom{

    public static boolean pairSum2(ArrayList<Integer> list, int target){
        int bp=-1;
        int n=list.size();
        for(int i=0; i<list.size()-1; i++){
            if(list.get(i)>list.get(i+1)){
                bp=i;
                break;
            }
        }
        int lp=bp+1;
        int rp=bp;
        while(lp != rp){
            if(list.get(lp) + list.get(rp)==target){
                return true;
            }else if(list.get(lp) + list.get(rp)<target){
                lp=(lp+1)%n;
            }else{
                rp=(n+rp-1)%n;
            }
        }
        return false;
    }
    public static void main(String args[]){
        ArrayList<Integer> list= new ArrayList<>();
        list.add(11);
        list.add(15);
        list.add(6);
        list.add(8);
        list.add(9);
        list.add(10); 
        System.out.println(list);
        System.out.println(pairSum2(list,10));
    }
}

-------------------------------ASSIGNMENT QUESTION {ARRAYLIST}-----------------------------------

// Q.101 -->
Question 1 :
Monotonic ArrayList (EASY)
An Arraylist is monotonic if it is either monotone increasing or monotone decreasing.
An Arraylist nums is monotone increasing if for all i <= j, nums.get(i) <= nums.get(j). An
Arraylist nums is monotone decreasing if for all i <= j, nums.get(i) >= nums.get(j).
Given an integer Arraylist nums, return true if the given list is monotonic, or false otherwise.

Sample Input 1 : nums = [1,2,2,3]
Sample Output 1 : true

Sample Input 2 : nums = [6,5,4,4]
Sample Output 2 : true

Sample Input 3 : nums = [1,3,2]
Sample Output 3 : false


import java.util.ArrayList;
public class ClassRoom{

    public static boolean isMonotonic(ArrayList<Integer> nums){
        boolean inc=true;
        boolean dec=true;
        for(int i=0; i<nums.size()-1; i++){
            if(nums.get(i) > nums.get(i+1)){
                inc = false;
            } 
            if(nums.get(i) < nums.get(i+1)){
                dec = false;
            }
        }
        return inc || dec;
    }

    public static void main(String args[]){
        ArrayList <Integer> nums= new ArrayList<>();
        nums.add(1);
        nums.add(2);
        nums.add(2);
        nums.add(4);
        System.out.println(nums);
        System.out.println(isMonotonic(nums));
    }
}

// Q.102 -->
Question 2 :
Lonely Numbers in ArrayList (MEDIUM)
You are given an integer arraylist nums. A number x is lonely when it appears only once, and
no adjacent numbers (i.e. x + 1 and x - 1) appear in the arraylist.
Return all lonely numbers in nums. You may return the answer in any order.

Sample Input 1 : nums = [10,6,5,8]
Sample Output 1 : [10,8]

Explanation :- 10 is a lonely number since it appears exactly once and 9 and 11 does not appear in nums.- 8 is a lonely number since it appears exactly once and 7 and 9 does not appear in nums.
raushanku914226@gmail.com- 5 is not a lonely number since 6 appears in nums and vice versa.
Hence, the lonely numbers in nums are [10, 8].
Note that [8, 10] may also be returned.

Sample Input 2 : nums = [1,3,5,3]
Sample Output 2 : [1,5]

Explanation :- 1 is a lonely number since it appears exactly once and 0 and 2 does not appear in nums.- 5 is a lonely number since it appears exactly once and 4 and 6 does not appear in nums.- 3 is not a lonely number since it appears twice.
Hence, the lonely numbers in nums are [1, 5].
Note that [5, 1] may also be returned.

Constraints :
● 1 <= nums.size() <= 105
● 0 <= nums.get(i) <= 106

import java.util.ArrayList;
import java.util.Collections;
public class ClassRoom{

    //O(nlogn)
    public static ArrayList<Integer> findLonelyNum(ArrayList<Integer> nums){
        ArrayList<Integer> soln=new ArrayList<>();
        if(nums==null || nums.isEmpty()){
            return soln;
        }
        //if there is single elt 
        if(nums.size()==1){
            soln.add(nums.get(0));
            return soln;
        }
        //sort the ArrayList
        Collections.sort(nums);

        //first elt 
        if(nums.get(1)-nums.get(0) > 1){
            soln.add(nums.get(0));
        }
        //middle elts
        for(int i=1; i<nums.size()-1; i++){
            if(nums.get(i)-nums.get(i-1) > 1 && nums.get(i+1)-nums.get(i) > 1){
                soln.add(nums.get(i));
            }
        }
        //last elt
        int n=nums.size();
        if(nums.get(n-1)-nums.get(n-2) > 1){
            soln.add(nums.get(n-1));
        }
        return soln;
    }

    public static void main(String args[]){
        ArrayList <Integer> nums= new ArrayList<>();
        nums.add(10);
        nums.add(6);
        nums.add(5);
        nums.add(8);
        System.out.println(nums);
        System.out.println(findLonelyNum(nums));
    }
}

// Q.103 -->
Question 3 :
Most Frequent Number following Key (EASY)
You are given an integer Arraylist nums. You are also given an integer key, which is present in
nums.

For every unique integer target in nums, count the number of times target immediately follows
an occurrence of key in nums. In other words, count the number of indices i such that:
0 <= i <= nums.size() - 2,
nums.get(i) == key and,
nums.get(i+1) == target.
Return the target with the maximum count.
(Assumption- that the target with maximum count is unique.)

Sample Input 1 :nums = [1,100,200,1,100], key = 1
Sample Output 1 :  100

Explanation :
For target = 100, there are 2 occurrences at indices 1 and 4 which follow an occurrence of key.
No other integers follow an occurrence of key, so we return 100.

Sample Input 2 : nums = [2,2,2,2,3], key = 2
Sample Output 2 :  2

Explanation :
For target = 2, there are 3 occurrences at indices 1, 2, and 3 which follow an occurrence of key.
For target = 3, there is only one occurrence at index 4 which follows an occurrence of key.
target = 2 has the maximum number of occurrences following an occurrence of key, so we
return 2.

Constraints :
● 2 <= nums.size() <= 1000
● 1 <= nums.get(i) <= 1000
● Assume that the answer is unique.

Hints : Count the number of times each target value follows the key in the arraylist.
Choose the target with the maximum count and return it.

import java.util.ArrayList;
public class ClassRoom{

    public static int mostFreqNumFollKey(ArrayList<Integer> nums, int key){
        int counts[]=new int[1001];
        int maxCount=Integer.MIN_VALUE;
        int ans=0;
        for(int i=0; i<nums.size()-1; i++){
            if(nums.get(i)==key){
                int target=nums.get(i+1);
                counts[target]++;

                if(counts[target] > maxCount){
                    maxCount=counts[target];
                    ans=target;
                }
            }
        }
        return ans;
    }

    public static void main(String args[]){
        ArrayList <Integer> nums= new ArrayList<>();
        nums.add(2);
        nums.add(20);
        nums.add(2);
        nums.add(30);
        nums.add(2);
        nums.add(30);

        int key=2;
        System.out.println(nums);
        System.out.println("Most frequent number is: "+mostFreqNumFollKey(nums,key));
    }
}

// Q.104 -->
Question 4 :
Beautiful ArrayList (MEDIUM)
An Arraylist nums of size n is beautiful if:

Sample Input 1 : n = 4
Sample Output 1 :  [2,1,4,3]

nums is a permutation of the integers in the range [1, n].
For every 0 <= i < j < n, there is no index k with i < k < j where 2 * nums.get(k) == nums.get(i) +
nums.get(j).
Given the integer n, return any beautiful arraylist nums of size n. There will be at least one valid
answer for the given n.

Sample Input 2 : n = 5
Sample Output 2 :  [3,1,2,5,4]

Constraints :
● 1 <= n <= 1000

//I WAS UNABLE TO SOLVE AND UNDERSTAND THE SOLUTION AT THIS TIME DON'T KNOW WHY...., AFTER GIVING TWO DAYS AND SEEING THE SOLUTIN.
import java.util.ArrayList;
public class ClassRoom{ 

    public static ArrayList<Integer> beautifulArrayList(int n){
        ArrayList<Integer> ans = new ArrayList<>(); 
        ans.add(1);
        
        while(ans.size() < 4){
            ArrayList<Integer> temp =new ArrayList<>();
            //odd elt
            for(int x:ans){
                if(2*x-1 <= n){
                    temp.add(2*x-1);
                }
            }
            //even elt
            for(int x:ans){
                if(2*x <=n){
                    temp.add(2*x);
                }
            }
            ans=temp;
        }
        return ans;
    }
    public static void main(String args[]){
        int n=4;
        System.out.println(beautifulArrayList(n));
    }
}

-------------------------------OR----------------------------------

import java.util.ArrayList;
public class ClassRoom{ 

    public ArrayList<Integer> beautifulArrayList(int n){
        ArrayList<Integer> res = new ArrayList<>(); 
        divideConquer(1, 1, res, n);
        return res;
    }

    private void divideConquer(int start, int increment, ArrayList<Integer> res, int n){
        if(start + increment >n){
            res.add(start);
            return;
        }
        divideConquer(start ,2*increment, res, n);
        divideConquer(start + increment, 2*increment, res, n);
    }
    public static void main(String args[]){
        int n=4;
        System.out.println(new ClassRoom().beautifulArrayList(n));
    }
}

--------------------------------------LINKED LIST ( PART 1 )----------------------------------------------

//Q. --> CREATION & OPERATION IN LINKED LIST.
public class LinkedList {

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data=data;
            this.next=null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    //T.C --> O(1)
    public void addFirst(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    //T.C --> O(1)
    public void addLast(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    //T.C --> O(n)
    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    //T.C --> O(n)
    public void add(int idx, int data){
        if(idx==0){
            addFirst(data);
            return;
        }
        Node temp = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            temp = temp.next;
            i++;
        }
        newNode.next = temp.next;
        temp.next = newNode;
    }
    
    public int removeFirst(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE; 
        }else if(size==1){
            int val = head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head=head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE;
        }else if(size==1){
            int val = tail.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp= head;
        int i=0;
        while(i < size-2){
            temp=temp.next;
            i++;
        }
        tail = temp;
        int val = tail.next.data;
        tail.next = null;
        size--;
        return val;
    }
    public static void main(String args[]){
        LinkedList ll =new LinkedList();
        //ll.print();
        ll.addFirst(2);
        //ll.print();
        ll.addFirst(1);
        //ll.print();
        ll.addLast(3);
        //ll.print();
        ll.addLast(4);
        //ll.print();
        ll.add(2,9);
        //ll.print();
        System.out.println(ll.size);
        ll.removeFirst();
        ll.print();
        System.out.println(ll.size);
        ll.removeLast();
        ll.print();
        System.out.println(ll.size);
    }
}

// Q.105 --> SEARCH (ITERATIVE) IN A LINKED LIST.

public class LinkedList {

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data=data;
            this.next=null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    //T.C --> O(1)
    public void addFirst(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    //T.C --> O(1)
    public void addLast(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    //T.C --> O(n)
    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    //T.C --> O(n)
    public void add(int idx, int data){
        if(idx==0){
            addFirst(data);
            return;
        }
        Node temp = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            temp = temp.next;
            i++;
        }
        newNode.next = temp.next;
        temp.next = newNode;
    }
    
    public int removeFirst(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE; 
        }else if(size==1){
            int val = head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head=head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE;
        }else if(size==1){
            int val = tail.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp= head;
        int i=0;
        while(i < size-2){
            temp=temp.next;
            i++;
        }
        tail = temp;
        int val = tail.next.data;
        tail.next = null;
        size--;
        return val;
    }

    public int itrSearch(int key){
        Node temp = head;
        for(int i=0; i<size; i++){
            if(temp.data == key){
                return i;
            }
            temp = temp.next;
        }
        return -1;
    }
    public static void main(String args[]){
        LinkedList ll =new LinkedList(); 
        ll.addFirst(2);      
        ll.addFirst(1);
        ll.addLast(3);
        ll.addLast(4);
        ll.add(2,9);
        ll.removeFirst();
        ll.removeLast();
        ll.addFirst(1);
        ll.addLast(4);
        ll.addLast(5);
        ll.print();
        System.out.println("Key is at idx: "+ll.itrSearch(10));
    }
}

// Q.106 --> SEARCH (RECURSIVE) IN A LINKED LIST.

public class LinkedList {

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data=data;
            this.next=null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    //T.C --> O(1)
    public void addFirst(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    //T.C --> O(1)
    public void addLast(int data){
        Node newNode =new Node(data);
        size++;
        if(head==null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    //T.C --> O(n)
    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    //T.C --> O(n)
    public void add(int idx, int data){
        if(idx==0){
            addFirst(data);
            return;
        }
        Node temp = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            temp = temp.next;
            i++;
        }
        newNode.next = temp.next;
        temp.next = newNode;
    }
    
    public int removeFirst(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE; 
        }else if(size==1){
            int val = head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head=head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size==0){
            System.out.println("LL is empty");
            return Integer.MIN_VALUE;
        }else if(size==1){
            int val = tail.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp= head;
        int i=0;
        while(i < size-2){
            temp=temp.next;
            i++;
        }
        tail = temp;
        int val = tail.next.data;
        tail.next = null;
        size--;
        return val;
    }

    public int helper(Node head, int key){
        if(head == null){
            return -1;
        }
        if(head.data == key){
            return 0;
        }
        int idx = helper(head.next,key);
        if(idx == -1){
            return -1;
        }
        return idx + 1;
    }

    public int recSearch(int key){
        return helper(head,key);
    }
    
    public static void main(String args[]){
        LinkedList ll =new LinkedList(); 
        ll.addFirst(2);      
        ll.addFirst(1);
        ll.addLast(3);
        ll.addLast(4);
        ll.add(2,9);
        ll.removeFirst();
        ll.removeLast();
        ll.addFirst(1);
        ll.addLast(4);
        ll.addLast(5);
        ll.print();
        System.out.println("Key is at idx: "+ll.recSearch(9));
    }
}


// Q.107 --> REVERSE A LINKEDLIST (ITERATIVE).

public class LinkedList{
    public static class Node{
    
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addFirst(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    public void add(int idx,int data){
        if(idx ==0){
            addFirst(data);
            return;
        }
        Node temp = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            temp = temp.next;
            i++;
        }
        newNode.next = temp.next;
        temp.next = newNode;
    }

    public int removeFirst(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head = head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp = head;
        int i=0;
        while(i < size -2){
            temp = temp.next;
            i++;
        }
        int val = tail.data;
        tail = temp;
        tail.next = null;
        size--;
        return val;
    }

    public int remove(int idx){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp = head;
        int i=0;
        while(i < idx-1){
            temp = temp.next;
            i++;
        }
        int val = temp.next.data;
        temp.next = temp.next.next;
        size--;
        return val;
    }

    public void reverse(){
        Node prev = null;
        Node curr = tail = head;
        Node next;

        while(curr != null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        head = prev;
    }

    public static void main(String args[]){
        LinkedList ll = new LinkedList();
        ll.addFirst(2);
        ll.addFirst(1);
        ll.addLast(3);
        ll.addLast(4);
        ll.addLast(5);
        ll.addLast(6);
        ll.print();
        ll.reverse();
        ll.print();
    }
}


// Q.108 --> FIND & REMOVE Nth NODE FROM END (ITERATIVE).

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addFirst(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    public void add(int idx,int data){
        if(idx ==0){
            addFirst(data);
            return;
        }
        Node prev = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            prev = prev.next;
            i++;
        }
        newNode.next = prev.next;
        prev.next = newNode;
    }

    public int removeFirst(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head = head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp = head;
        int i=0;
        while(i < size -2){
            temp = temp.next;
            i++;
        }
        int val = tail.data;
        tail = temp;
        tail.next = null;
        size--;
        return val;
    }

    public int remove(int idx){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node prev = head;
        int i=0;
        while(i < idx-1){
            prev = prev.next;
            i++;
        }
        int val = prev.next.data;
        prev.next = prev.next.next;
        size--;
        return val;
    }

    public void reverse(){
        Node prev = null;
        Node curr = tail = head;
        Node next;

        while(curr != null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        head = prev;
    }

    // public void removeNthFromEnd(int idx){
    //     reverse();
    //     remove(idx);
    //     reverse();
    // }

    public int removeNthFromEnd(int n){
        int sz = 0;
        Node temp = head;
        while(temp != null){
            temp = temp.next;
            sz++;
        }
        if(sz == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(sz == 1){
            int val = head.data;
            head = tail = null;
            return val;
        }
        if(n == sz){
            int val = head.data;
            head = head.next;
            return val;
        }
        Node prev = head;
        int i=1;
        while(i < sz - n){
            prev = prev.next;
            i++;
        }
        int val = prev.next.data;
        prev.next = prev.next.next;
        return val;
    }

    public static void main(String args[]){
        LinkedList ll = new LinkedList();
        ll.addFirst(2);
        ll.addFirst(1);
        ll.addLast(3);
        ll.addLast(4);
        ll.addLast(5);
        ll.addLast(6);
        ll.print();
        ll.removeNthFromEnd(3);
        ll.print();
    }
}

// Q.109 --> CHECK IF A LINKEDLIST IS A PALINDROME.

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addFirst(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head = newNode;
    }

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    public void print(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    public void add(int idx,int data){
        if(idx ==0){
            addFirst(data);
            return;
        }
        Node prev = head;
        Node newNode = new Node(data);
        size++;
        int i=0;
        while(i < idx-1){
            prev = prev.next;
            i++;
        }
        newNode.next = prev.next;
        prev.next = newNode;
    }

    public int removeFirst(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        int val = head.data;
        head = head.next;
        size--;
        return val;
    }

    public int removeLast(){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node temp = head;
        int i=0;
        while(i < size -2){
            temp = temp.next;
            i++;
        }
        int val = tail.data;
        tail = temp;
        tail.next = null;
        size--;
        return val;
    }

    public int remove(int idx){
        if(size == 0){
            System.out.println("LinkedList is empty");
            return Integer.MIN_VALUE;
        }else if(size == 1){
            int val =head.data;
            head = tail = null;
            size = 0;
            return val;
        }
        Node prev = head;
        int i=0;
        while(i < idx-1){
            prev = prev.next;
            i++;
        }
        int val = prev.next.data;
        prev.next = prev.next.next;
        size--;
        return val;
    }

    public Node findMid(Node head){
        Node slow =head;
        Node fast = head;
        while(fast != null && fast.next != null){
            slow = slow.next;
            fast = fast.next.next;
        }
        return slow;
    }

    public boolean isPalindrome(){
        Node midNode = findMid(head);
        Node prev = null;
        Node curr = midNode;
        Node next;
        while(curr != null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        Node right = prev; //right half LL's head
        Node left = head;
        while(right != null ){
            if(left.data != right.data){
                return false;
            }
            left = left.next;
            right = right.next;
        }
        return true;
    }

    public static void main(String args[]){
        LinkedList ll = new LinkedList();
        ll.addFirst(2);
        ll.addFirst(1);
        ll.addLast(2);
        ll.addLast(1);
        ll.print();
        System.out.println(ll.isPalindrome());
    }
}

--------------------------------------LINKED LIST ( PART 2 )----------------------------------------------

// Q. --> DETECT A LOOP/CYCLE IN A LINKED LIST.

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public static boolean isCycle(){
        Node slow = head;
        Node fast = head;
        while(fast != null && fast.next != null){
            slow = slow.next;
            fast = fast.next.next;
            if(fast == slow){
                return true;
            }
        }
        return false;
    }

    public static void main(String args[]){
        head = new Node(1);
        head.next = new Node(2);
        head.next.next = new Node(3);
        head.next.next.next = new Node(4);
        head.next.next.next.next = head;
        System.out.println(isCycle());
    }
}

// Q.110 -->  REMOVE A LOOP/CYCLE IN A LINKED LIST.

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public static void removeCycle(){

        //detect cycle
        Node slow = head;
        Node fast = head;
        boolean cycle = false;
        while(fast != null && fast.next != null){
            slow = slow.next; //+1
            fast = fast.next.next; //+2
            if(fast == slow){
                cycle = true;
                break;
            }
        }

        if(cycle == false){
            return;
        }

        //find meeting point
        slow = head;
        Node prev = fast;
        while(fast != slow){
            slow = slow.next; //+1
            prev = fast;
            fast = fast.next; //+1
        }

        //remove cycle
        prev.next = null;
    }

    public static void main(String args[]){
        head = new Node(1);
        System.out.print(head.data+" --> ");

        head.next = new Node(2);
        System.out.print(head.next.data+" --> ");

        Node temp = new Node(3);
        System.out.print(temp.data+" --> ");

        head.next.next = temp;
        head.next.next.next = new Node(4);
        System.out.print(head.next.next.next.data+" --> ");

        head.next.next.next.next = temp;
        System.out.println(head.next.next.next.next.data);


        System.out.println("isCycle: "+isCycle());
        if(isCycle()){
            removeCycle();
            System.out.println("isCycle: "+isCycle());
        }
    }
}

//Q.111 --> APPLY MERGE SORT ON A LINKED LIST.

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

        public void addLast(int data){
            Node newNode = new Node(data);
            size++;
            if(head == null){
                head = tail = newNode;
                return;
            }
            tail.next = newNode;
            tail = newNode;
        }

        public void print(){
            Node temp = head;
            while(temp != null){
                System.out.print(temp.data+" --> ");
                temp = temp.next;
            }System.out.println("null");
        }

        public Node findMid(Node head){
            Node slow = head;
            Node fast = head.next;
            while(fast != null && fast.next != null){
                slow = slow.next;
                fast = fast.next.next;
            }
            return slow;
        }

        public Node mergeSort(Node head){
            if(head == null || head.next == null){
                return head;
            }
            Node mid = findMid(head);
            Node rightHead = mid.next;
            mid.next = null;

            Node newLeft = mergeSort(head);
            Node newRight = mergeSort(rightHead);
            
            return  merge(newLeft, newRight);
        }

        public Node merge(Node head1,Node head2){
            Node mergedLL = new Node(-1);
            Node temp = mergedLL;

            while(head1 != null && head2 != null){
                if(head1.data <= head2.data){
                    temp.next = head1;
                    head1 = head1.next;
                    temp = temp.next;
                }else{
                    temp.next = head2;
                    head2 = head2.next;
                    temp = temp.next;
                }
            }
            while(head1 != null){
                temp.next = head1;
                head1 = head1.next;
                temp = temp.next;
            }
            while(head2 != null){
                temp.next = head2;
                head2 = head2.next;
                temp = temp.next;
            }

            return mergedLL.next;
        }

        public static void main(String args[]){
            LinkedList ll = new LinkedList();
            ll.addLast(8);
            ll.addLast(2);
            ll.addLast(5);
            ll.addLast(6);
            ll.addLast(1);
            ll.addLast(7);
            ll.print();
            ll.head = ll.mergeSort(ll.head);
            ll.print();
        }
}

//Q.112 --> ZIG-ZAG LINKED LIST.
FOR A LNKEDLIST OF THE FORM: L(1)->L(2)->L(3)->L(4)....L(n-1)->L(n). CONVERT IT INTO ZIG-ZAG FORM i.e L(1)->L(n)->L(2)->L(n-1)->L(3)-L(n-2)......

<img width="647" height="307" alt="image" src="https://github.com/user-attachments/assets/cbcce606-c1ec-49ae-9a78-2fd0be4ef47b" />

public class LinkedList{

    //MY APPROACH -> CORRECT SAHI H
    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

        public void addLast(int data){
            Node newNode = new Node(data);
            size++;
            if(head == null){
                head = tail = newNode;
                return;
            }
            tail.next = newNode;
            tail = newNode;
        }

        public void print(){
            System.out.println();
            Node temp = head;
            while(temp != null){
                System.out.print(temp.data+" --> ");
                temp = temp.next;
            }System.out.println("null");
        }

        public Node reverse(Node head){
            Node curr = head;
            Node prev = null;
            Node next;

            while(curr != null){
                next = curr.next;
                curr.next = prev;
                prev = curr;
                curr = next;
            }
            head = prev;

            return head;
        }

        private Node findMid(Node head){
            Node slow = head;
            Node fast = head.next;

            while(fast != null && fast.next != null){
                slow = slow.next;
                fast = fast.next.next;
            }

            return slow;
        }

        public Node zigZagLL(Node head){
            if( head == null || head.next == null){
                return head;
            }

            Node mid = findMid(head);
            Node rightHead = mid.next;
            mid.next = null;
            
            Node leftLL = head;
            Node rightLL = reverse(rightHead);

            return alternateMerging(leftLL, rightLL);
        }

        public Node alternateMerging(Node head1, Node head2){
            Node mergedLL = new Node(-1);
            Node temp = mergedLL;

            while(head1 != null && head2 != null){
                temp.next = head1;
                head1 = head1.next;
                temp = temp.next;

                temp.next = head2;
                head2 = head2.next;
                temp = temp.next;
            }

            if(head1 != null){
                temp.next = head1;
                temp = temp.next;
            }
            
            tail = temp;

            return mergedLL.next;
        }
            

        public static void main(String args[]){
            LinkedList ll = new LinkedList();
            ll.addLast(1);
            ll.addLast(2);
            ll.addLast(3);
            ll.addLast(4);
            ll.addLast(5);
            ll.print();
            //ll.head = ll.reverse(ll.head);
            ll.head = ll.zigZagLL(ll.head);
            ll.print();
        }
}

----------------------DEDICATED FOR ZIG-ZAG LL---------------------------

public class LinkedList{

    public static class Node{
        int data;
        Node next;

        public Node(int data){
            this.data = data;
            this.next = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        tail = newNode;
    }

    public void print(){
        System.out.println();
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" --> ");
            temp = temp.next;
        }System.out.println("null");
    }

    public Node reverse(Node head){
        Node curr = head;
        Node prev = null;
        Node next;

        while(curr != null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        head = prev;

        return head;
    }

    private Node findMid(Node head){
        Node slow = head;
        Node fast = head.next;

        while(fast != null && fast.next != null){
            slow = slow.next;
            fast = fast.next.next;
        }

        return slow;
    }

    public void zigZagLL(){
        //find mid
        Node mid = findMid(head);
        //2nd half
        Node rightHead = mid.next;
        mid.next = null;
        
        Node leftHd = head;
        Node rightHd = reverse(rightHead);

        //Alternate Merging
        Node nextL,nextR;
        while(leftHd != null && rightHd != null){
            nextL = leftHd.next;
            leftHd.next = rightHd;
            nextR = rightHd.next;
            rightHd.next = nextL;

            leftHd = nextL;
            rightHd = nextR;
        }
    }
        

    public static void main(String args[]){
        LinkedList ll = new LinkedList();
        ll.addLast(1);
        ll.addLast(2);
        ll.addLast(3);
        ll.addLast(4);
        ll.addLast(5);
        ll.print();
        //ll.head = ll.reverse(ll.head);
        ll.zigZagLL();
        ll.print();
    }
}

//Q. --> CREATION & OPERATION IN DOUBLE LINKED LIST.

public class LinkedList{

    public class Node{
        int data;
        Node next;
        Node prev;

        public Node(int data){
            this.data = data;
            this.next = null;
            this.prev = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addFirst(int data){
        Node newNode = new Node(data);
        size++;

        if(head == null){
            head = tail = newNode;
            return;
        }

        newNode.next = head;
        head.prev = newNode;
        head = newNode;
    }

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;

        if(head == null){
            head = tail = newNode;
            return;
        }

        tail.next = newNode;
        newNode.prev = tail;
        tail = newNode;
    }

    public void print() {
        if (head == null) {
            System.out.println("null");
            return;
        }
        Node temp = head;
        System.out.print("null <-- ");
        while (temp != null) {
            System.out.print(temp.data);
            if (temp.next != null) {
                System.out.print(" <--> ");
            } else {
                System.out.print(" --> null");
            }
            temp = temp.next;
        }
        System.out.println();
    }

    public int removeFirst(){
        if(head == null){
            System.out.println("Double LL is empty");
            return Integer.MIN_VALUE;
        }

        if(head == tail){  //single element
            int val = head.data;
            head = tail = null;
            size--;
            return val;
        }

        int val = head.data;
        head = head.next;
        head.prev = null;
        size--;
        return val;
    }

    public int removeLast(){
        if(head == null){
            System.out.println("Double LL is empty");
            return Integer.MIN_VALUE;
        }

        if(head == tail){  //single element
            int val = head.data;
            head = tail = null;
            size--;
            return val;
        }

        int val = tail.data;
        tail = tail.prev;
        tail.next = null;
        size--;
        return val;
    }

    public static void main(String args[]){
        LinkedList dll = new LinkedList();
        dll.addFirst(4);
        dll.addFirst(3);
        dll.addFirst(2);
        dll.addFirst(1);
        dll.addLast(5);
        dll.addLast(6);
        dll.addLast(7);
        dll.print();
        System.out.println("size: "+dll.size);
        System.out.println("\nremoved Node: "+dll.removeFirst());
        dll.print();
        System.out.println("size: "+dll.size);
        System.out.println("\nremoved Node: "+dll.removeLast());
        dll.print();
        System.out.println("size: "+dll.size);
    }
}

//Q. --> REVERSE A DOUBLE LINKED LIST.

public class LinkedList{

    public class Node{
        int data;
        Node next;
        Node prev;

        public Node(int data){
            this.data = data;
            this.next = null;
            this.prev = null;
        }
    }
    public static Node head;
    public static Node tail;
    public static int size;

    public void addFirst(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head.prev = newNode;
        head = newNode;
    }

    public void addLast(int data){
        Node newNode = new Node(data);
        size++;
        if(head == null){
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        newNode.prev = tail;
        tail = newNode;
    }

    public void print() {
        if (head == null) {
            System.out.println("null");
            return;
        }
        Node temp = head;
        System.out.print("null <-- ");
        while (temp != null) {
            System.out.print(temp.data);
            if (temp.next != null) {
                System.out.print(" <--> ");
            } else {
                System.out.print(" --> null");
            }
            temp = temp.next;
        }
        System.out.println();
    }

    public void reverse(){
        Node curr = head;
        Node prev = null;
        Node next;
        while(curr != null){
            next = curr.next;
            curr.next = prev;
            curr.prev = next;
            prev = curr;
            curr = next;
        }
        head = prev;
    }

    public static void main(String args[]){
        LinkedList dll = new LinkedList();
        dll.addFirst(4);
        dll.addFirst(3);
        dll.addFirst(2);
        dll.addFirst(1);
        dll.addLast(5);
        dll.addLast(6);
        dll.addLast(7);
        dll.print();
        dll.reverse();
        dll.print();
    }
}
