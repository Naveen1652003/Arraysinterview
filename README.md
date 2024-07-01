# Arraysinterview
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int arr[] = {1, 2, 2, 3, 4, 5,5,7,8,9,10};
        int arr1[] = {5, 6, 7, 1, 2,6,7,8,9};
        int n = arr.length + arr1.length;
        int res[] = new int[n];
      
        for(int i = 0; i < arr.length; i++) {
            res[i] = arr[i];
        }
        for(int i = 0; i < arr1.length; i++) {
            res[i + arr.length] = arr1[i];
        }
        Arrays.sort(res);
        System.out.print("Sorted Merged Array: ");
        for(int i = 0; i < res.length; i++) 
        {
            System.out.print(res[i] + " ");
        }
        System.out.println();
        System.out.print(res[0] + " ");
        for(int i = 1; i < res.length; i++) 
        {
            if(res[i] != res[i-1]) 
            {
                System.out.print(res[i] + " ");
            }
        }
    }
}
ouput:

arr={1,,2,2,3,4,5}
arr1={5,6,7,1,2}
output is{1,2,3,4,5,6}    merge two array

