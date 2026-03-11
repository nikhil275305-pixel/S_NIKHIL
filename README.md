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


