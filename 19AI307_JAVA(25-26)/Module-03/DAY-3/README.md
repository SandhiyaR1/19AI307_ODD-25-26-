# Ex.No:3(C) ABSTRACTION

## QUESTION:
Write a Java program that defines an abstract class SignalAgent with an abstract method decodeSignal(int[] signal). Create two subclasses PrimeAgent and MirrorAgent that implement different decoding strategies:

PrimeAgent → returns the sum of all prime numbers in the signal.

MirrorAgent → checks if the signal is perfectly symmetric; if yes return 1, else return 0.

## AIM:
To design a Java program using abstraction and inheritance where an abstract class SignalAgent provides a decoding interface, and two subclasses (PrimeAgent and MirrorAgent) implement different decoding mechanisms for processing alien numerical signals.

## ALGORITHM :
1. Start the program.
2. Create an abstract class SignalAgent

Contains abstract method: int decodeSignal(int[] signal).

3. Create class PrimeAgent extending SignalAgent

Traverse the array.

Check each element for primality.

If prime, add it to a running sum.

Return the sum.

4. Create class MirrorAgent extending SignalAgent

Use two pointers: start (left) and end (right).

Compare elements at both ends while moving inward.

If all matching pairs are equal → return 1 (balanced).

Else → return 0 (not symmetric).

5. In main():

Input a signal (array of integers).

Create objects of PrimeAgent and MirrorAgent.

Call decodeSignal() on each and display the results.

6. End the program.




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class SignalAgent
{
    abstract int decodeSignal(int[] signal);
}
class PrimeAgent extends SignalAgent{
    @Override
    int decodeSignal(int[] signal)
    {
        int sum=0;
        int i;
        for(i=0;i<signal.length;i++)
        {
           boolean isPrime=true;
           
           for(int j=2;j<signal[i];j++)
           {
               if(signal[i]%j==0)
               {
                   isPrime=false;
               }
           }
           if(isPrime)
           {
               sum+=signal[i];
           }
        }
        return sum;
    }
}
class MirrorAgent extends SignalAgent{
    @Override
    int decodeSignal(int[] signal)
    {
        for(int i=0;i<signal.length/2;i++)
        {
            if(signal[i]!=signal[signal.length-i-1])
            {
                return 2;
            }
        }
        return 1;
    }
}
public class Main{
    public static void main(String arg[])
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        int i;
        for(i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        int choice=sc.nextInt();
        if(choice==1)
        {
            PrimeAgent p=new PrimeAgent();
            System.out.println(p.decodeSignal(arr));
        }
        else
        {
            MirrorAgent m=new MirrorAgent();
            if(m.decodeSignal(arr)==1){
            System.out.println("BALANCED");
        }
        else if(m.decodeSignal(arr)==2)
        {
            
            System.out.println("BROKEN");
        }
        }
    }
}
```


## OUTPUT:


<img width="458" height="303" alt="image" src="https://github.com/user-attachments/assets/1c6c8610-7605-4f8b-9d5d-0b8f16bcdf78" />


## RESULT:

The program successfully demonstrates abstraction and polymorphism using the SignalAgent abstract class.
PrimeAgent accurately sums all prime numbers in the signal, while MirrorAgent correctly determines whether the signal is symmetric.
Thus, both agents decode the mysterious alien signal according to their own intelligent rules.

