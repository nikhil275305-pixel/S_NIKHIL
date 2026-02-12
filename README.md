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
---------------------------

Q. RECTANGLE (HOLLOW) SHAPE WITH STAR.
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

Q. HALF PYRAMID WITH STAR.
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

Q. INVERTED & ROTATED HALF PYRAMID WITH STAR.
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

Q. INVERTED HALF PYRAMID WITH NUMNBERS.
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

Q. FLOYD'S TRIANGLE.
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

Q. 0-1 TRIANGLE.
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

Q. BUTTERFLY PATTERN.
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

Q. SOLID RHOMBUS PATTERN.
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

Q. HOLLOW RHOMBUS PATTERN.
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

          
