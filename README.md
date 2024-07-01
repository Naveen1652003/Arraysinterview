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





//////////////////////////////////////////////zigzag program//////////////////////////////////////////////


package logicprogra;
import java.util.*;
public class Sumofnumberandproduct 
{

	public static void main(String[] args) 
	{
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		int temp=0;
		int sum=0;
		int pro=1;
		
		while(n>0)
		{
			temp=n%10;
			sum=sum+temp;
			pro=pro*temp;
			n=n/10;
			
		}
		System.out.println(sum);
		System.out.println(pro);
		
	}

}


//////////////////////////////////////////// zig program////////////////////////////////////////////////////

package logicprogra;
import java.util.*;
public class Zigprogram {
	
	public static int len(int num)
	{
		int count=0;
		while(num!=0)
		{
			num=num/10;
			count++;
		}
		return count;
	}
	
	public static int rev(int num)
	{
		int rev=0;
		while(num!=0)
		{
			int d=num%10;
			rev=rev*10+d;
			num=num/10;
		}
		return rev;
		
	}

	public static void main(String[] args) 
	{
		Scanner sc=new Scanner(System.in);
		int num1=sc.nextInt();
		int num2=sc.nextInt();
		if(len(num1)==len(num2))
		{
			int rev1ofnum=rev(num1);
			int zig=0;
			while(rev1ofnum!=0)
			{
				int d=rev1ofnum%10;
				zig=zig*10+d;
				
				d=num2%10;
				zig=zig*10+d;
				rev1ofnum=rev1ofnum/10;
				num2=num2/10;
			}
			System.out.println(zig);
			
		}
		else
		{
			System.out.println("Invalid");
		}
		
		
		
	}

}



