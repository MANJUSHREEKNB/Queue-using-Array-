# Queue-using-Array-
//Implement stack using Array 1
//SOURCE CODE

import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner (System.in);
        Stack s=new Stack();
        int n=sc.nextInt();
        for(int i=0;i<n;i++){
            String str=sc.next(); 
            if(str.equals("Push")){
                int val=sc.nextInt();
                s.push(val);
            }
            else if(str.equals("Pop")){
                s.pop();
            }
            else if(str.equals("Print")){
                s.print();
            }
        }
    }
}
class Stack{
    final int size=100;
    int arr[]=new int [size];    
    int top=-1;
    public void push(int val){
        arr[++top]=val;
    }
    public void pop(){
        top--;
    }
    public void print(){
        for(int i=0;i<=top;i++)
            System.out.println(arr[i]);
    }
}
