# [Video Link](https://youtu.be/TAtrPoaJ7gc)

## Write Java programs for the following:

1. Write a program to print whether a number is even or odd, also take
input from the user.
2. Take name as input and print a greeting message for that particular name.
3. Write a program to input principal, time, and rate (P, T, R) from the user and
find Simple Interest.
4. Take in two numbers and an operator (+, -, *, /) and calculate the value.
(Use if conditions)
5. Take 2 numbers as input and print the largest number.
6. Input currency in rupees and output in USD.
7. To calculate Fibonacci Series up to n numbers.
8. To find out whether the given String is Palindrome or not.
9. To find Armstrong Number between two given number.

 Write a program to print whether a number is even or odd, also take
 
import java.util.Scanner;
public class Even{
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter a Number:");
        int num = in.nextInt();
        if (num % 2 == 0){
            System.out.println("Even Number");
        }
        else{
            System.out.println("Odd Number");
        }
    }
}


2. Take name as input and print a greeting message for that particular name.
   
import java.util.Scanner;

public class Greetings {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.err.println("Enter the Name:");
        String name = in.nextLine();
        System.err.println("Happy Birthday " + name);
    }
}


3. Write a program to input principal, time, and rate (P, T, R) from the user and
find Simple Interest.

import java.util.Scanner;
public class Interest {
    public static void main(String[] args) {
        int principal,time,rate;
        float Interest;
        Scanner in = new Scanner(System.in);
        System.err.println("Enter Principal Amount:");
        principal = in.nextInt();
        System.err.println("Enter time:");
        time = in.nextInt();
        System.err.println("Enter Rate of Interest:");
        rate = in.nextInt();
        Interest = (principal*time*rate)/100;
        System.err.println("Total Interest is:" + Interest);
    }
}


4. Take in two numbers and an operator (+, -, *, /) and calculate the value.
(Use if conditions)
import java.util.Scanner;
public class Calculator {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int ans=0;
        while (true) { 
            System.out.println("Enter Num1 :");
            int num1 = in.nextInt();
            System.out.println("Enter Num2 :");
            int num2 = in.nextInt();
            System.out.println("Enter the operator:");
            char op = in.next().charAt(0);
            if(op=='+'){
                ans = num1 + num2;
            }
            if(op=='-'){
                ans = num1 - num2;
            }
            if(op=='*'){
                ans = num1 * num2;
            }
            if(op=='/'){
                ans = num1 / num2;
            }
            else if(op == 'x' || op == 'X'){
                break;
            }
            else{
                System.out.println("Invalid Operation");
            }
            System.out.println(ans);
        }
    }
    
}

5. Take 2 numbers as input and print the largest number.

import java.util.Scanner;
public class Largest {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter num1");
        int num1 = in.nextInt();
        System.out.println("Enter num2");
        int num2 = in.nextInt();
        int res = Math.max(num1, num2);
        System.out.println(res);  
    }
}

6. Input currency in rupees and output in USD.

import java.util.Scanner;
public class Rupees {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter Amount in Rupees:");
        float cash = in.nextFloat();
        double usd;
        usd = cash * 0.012;
        System.out.println("Amount in usd:" + usd + "$");
    }
}

7. To calculate Fibonacci Series up to n numbers.

mport java.util.Scanner;
public class Fibonacci_1 {
    public static void main(String[] args) {
        int n1=0,n2=1,n3,count;
        Scanner in = new Scanner(System.in);
        System.out.println("Enter the series:");
        count = in.nextInt();
        System.out.println(n1 + " "+n2);
        for(int i=2;i<=count;++i){
            n3 = n1 + n2;
            System.out.println(" "+n3);
            n1 = n2;
            n2 = n3;

        }
    }
}

8. To find out whether the given String is Palindrome or not.

import java.util.Scanner;
public class palindrome {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter a string:");
        String str = in.nextLine();
        int length = str.length();
        String rev = "";
        for(int i=length-1;i>=0;i--)
            rev = rev + str.charAt(i);
        if(str.equals(rev))
            System.out.println("Is a Palindrome");
        else{
                System.out.println("Not a Palindrome");
            }
    }
}

9. To find Armstrong Number between two given number.

import java.util.Scanner;

public class armstrong
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter lower and upper ranges : ");
        int low = sc.nextInt();
        int high = sc.nextInt();

        System.out.println("Armstrong numbers between "+ low + " and " + high + " are : ");

        // loop for finding and printing all armstrong numbers between given range
        for(int num = low ; num <= high ; num++)
        {
            int sum = 0, temp, digit, len;

            len = getOrder(num);
            temp = num;
            // loop to extract digit, find ordered power of digits & add to sum
            while(temp != 0)
            {
                // extract digit
                digit = temp % 10;

                // add power to sum
                sum = sum + (int) Math.pow(digit,len);
                temp /= 10;
            };

            if(sum == num)
                System.out.print(num + " ");
        }

    }

    private static int getOrder(int num) {
            int len = 0;
            while (num!=0)
            {
                len++;
                num = num/10;
            }
            return len;
    }
}
