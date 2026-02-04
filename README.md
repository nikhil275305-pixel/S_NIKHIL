# S_NIKHIL
This is my first Git Repository

Q_PRIME NUMBER FORM 1 TO N.
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

Q_BINARY TO DECIMAL.
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


Q_DECIMAL TO BINARY.
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
