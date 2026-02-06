# S_NIKHIL
This is my first Git Repository

Q. PRIME NUMBER FORM 1 TO N.
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

Q. BINARY TO DECIMAL.
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


Q. DECIMAL TO BINARY.
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

Q. SUM OF DIGITS OF THAT NUMBER.
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

Q. CHECK IF A NUBER IS PALINDROME.
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
          OR


          
