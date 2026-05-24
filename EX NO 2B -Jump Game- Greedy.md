
# EX 2B Jump Game using Greedy Algorithm.
## DATE:
## AIM:
To write a Java program to for given constraints.
You are given an array of integers. Each number represents the maximum number of steps you can jump forward from that position.

You start from the first element (index 0). 
Write a program to find the minimum number of jumps required to reach the last index of the array.

If it is not possible to reach the end, return -1.
## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to implement Reverse a String
Developed by: RENUSRI NARAHARASHETTY
Register Number:  212223240139
*/

import java.util.Scanner;

public class MinJumpToEnd {

    // Function to return minimum jumps to reach end
    public static int minimumJumps(int[] nums) {
        if(nums.length<=1) return 0;
        if(nums[0]==0) return -1;
        int jumps=0;
        int currentEnd=0;
        int farthest=0;
        for(int i=0;i<nums.length-1;i++){
            farthest=Math.max(farthest,i+nums[i]);
            if(i==currentEnd){
                jumps++;
                currentEnd=farthest;
            }
            if(currentEnd>nums.length-1) break;
            if(currentEnd==i) return -1;
        }
        return currentEnd>=nums.length-1?jumps:-1;
    }

    // Main method to handle input and output
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); // Number of elements
        int[] nums = new int[n];

        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }

        System.out.println("Minimum jumps to reach last index: " + minimumJumps(nums));
    }
}

```

## Output:
<img width="998" height="313" alt="image" src="https://github.com/user-attachments/assets/bc7144c9-2d87-4471-9fc3-8be9341c121e" />



## Result:
The program successfully implemented and the expected output is verified.
