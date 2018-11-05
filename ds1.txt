q1.)

import java.util.*;
public class QuestionOne{
	public static void getMax(int[] arr){
		int max=arr[0];
		for(int i:arr){
			if(i>max){max=i;}
		}
		System.out.println("Maximum -> " + max);
	}
	public static void main(String[] args){
		Scanner scan=new Scanner(System.in);
		System.out.print("Enter the number of elements : ");
		int n=scan.nextInt(); 
		int[] arr=new int[n];
		System.out.println("Enter elements");
		for(int i=0;i<n;i++){
			arr[i]=scan.nextInt();
		}
		QuestionOne.getMax(arr);
	}
}
--------------------------------------------------------
q2.)

import java.util.Scanner;
public class QuestionTwo
{
	private static void sort(int[] arr)
	{
		System.out.println(" Bubble Sorting the array...");
		for(int i=0;i<arr.length-1;i++)
		{
			for(int j=0;j<arr.length-i-1;j++)
			{
				if(arr[j] > arr[j+1])
				{
					int temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp;
				}
			}
		}
		
	}
	
	public static void main(String[] args)
	{
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter the number of elements : ");
		int N = sc.nextInt();
		int arr[] = new int[N];
		System.out.println("Start entering elements :-");
		for(int i=0;i<N;i++)
			arr[i] = sc.nextInt();
		
		System.out.println("\nThe entered array :-");
		for(int i=0;i<N;i++)
			System.out.print(arr[i] + " ");
		System.out.println();
		
		sort(arr);
		
		System.out.println("\nThe entered array :-");
		for(int i=0;i<N;i++)
			System.out.print(arr[i] + " ");
		System.out.println();
		
		System.out.println();
		sc.close();
	}
}
------------------------------------------------------------
q3.)

import java.util.*;
public class QuestionThree{
	public static void main(String[] args){
		Scanner scan=new Scanner(System.in);
		System.out.print("Enter the size of array : ");
		int n=scan.nextInt(); 
		int[] arr=new int[n];
		System.out.println("Enter elements");
		for(int i=0;i<n;i++){
			arr[i]=scan.nextInt();
		}
		
		System.out.print("Enter the size of second array : ");
		n=scan.nextInt(); 
		int[] ar=new int[n];
		System.out.println("Enter elements");
		for(int i=0;i<n;i++){
			ar[i]=scan.nextInt();
		}
		int length=ar.length>arr.length?ar.length:arr.length;
		int[] inter=new int[length];
		Arrays.sort(ar);
		Arrays.sort(arr);
		int c=0;
		for(int i=0;i<arr.length;i++){
			N:for(int j=c;j<ar.length;j++){
				if(arr[i]==ar[j]){
					inter[c++]=arr[i];
					break N;
				}
			}
		}
		System.out.println("INTERSECTION ARRAY");
		for(int i=0;i<c;i++){
			System.out.print(inter[i]+" ");
		}
	}
}
---------------------------------------------------------------------------
q4.)

import java.util.*;
public class QuestionFour{
	public static void main(String[] args){
		System.out.println("Enter size of array m * n");
		Scanner scan=new Scanner(System.in);
		int m=scan.nextInt();
		int n=scan.nextInt();
		int[][] arr=new int[m][n];
		for(int i=0;i<m;i++)
			for(int j=0;j<n;j++)
				arr[i][j] = scan.nextInt();
		
		int j=0;
		for(int i=0;i<m;i++){
			for(j=0;j<n;j++){
				System.out.print(arr[i][j]+",");
			}
			++i;
			if(i<m){
				for(j=n-1;j>=0;j--){
					System.out.print(arr[i][j]+",");
				}
			}
		}
	}
}
---------------------------------------------------------------------------
q5.)

import java.util.*;
public class QuestionFive{
	public static void main(String[] args){
		Scanner scan=new Scanner(System.in);
		System.out.print("Enter the number of elements : ");
		int n=scan.nextInt(); 
		int[] arr=new int[n];
		System.out.println("Enter elements");
		for(int i=0;i<n;i++){
			arr[i]=scan.nextInt();
		}
		int i=0,j=arr.length-1;
		while(i!=j && i<j){
			int t=arr[i];
			arr[i]=arr[j];
			arr[j]=t;
			i++;
			j--;
		}
		for(i=0;i<n;i++){
			System.out.print(arr[i]+" ");
		}
	}
}

