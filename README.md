# S_NIKHIL
This is my first Git Repository

Q.PRINT ALL PRIME NUMBER FORM 1 TO N.
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

Q.CONVERSION FROM BINARY TO DECIMAL.
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

