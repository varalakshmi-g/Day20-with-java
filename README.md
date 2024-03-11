
# Day20-with-java

Hey all it's my day20 of learning java

Today I am very happy that in single attempt my program got executed. Everyday it tooks not less than 10 attempts. 

Today's task is to print the elements along with its count value.

The program I practiced and learned today is here we goo...

import java.util.Scanner;
public class Day20 {
    static void  printOccurence(int[] ar) 
    {
        int count = 1;
        for(int i = 0; i < ar.length-1; i++)
        {
            if (ar[i] == ar[i+1])
            {
                count++;
                
            }
            else 
            {
                System.out.println(ar[i] + "-" + count);
                count = 1;
            }
        }
         System.out.println(ar[ar.length-1] + "-" + count);
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for(int i = 0; i < ar.length; i++) 
        {
            ar[i] = scan.nextInt();
        }
        
        printOccurence(ar);
        
    }
}

output:
No.of elements in array: 5
Elements are: 1 2 2 3 4
occurences:
1-1
2-2
3-1
4-1

with reference of the above program, we can write one more program that is to print all elements without repeating.

import java.util.Scanner;
public class Day20 {
    static void  printElementsWithoutRepeating(int[] ar) 
    {
        int count = 1;
        for(int i = 0; i < ar.length-1; i++)
        {
            if (ar[i] == ar[i+1])
            {
                count++;
                
            }
            else 
            {
                System.out.println(ar[i]);
                count = 1;
            }
        }
         System.out.println(ar[ar.length-1]);
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for(int i = 0; i < ar.length; i++) 
        {
            ar[i] = scan.nextInt();
        }
        
        printElementsWithoutRepeating(ar);
        
    }
}

out put:
No.of elements in array: 5
Elements are: 1 2 2 3 4
1
2
3
4




