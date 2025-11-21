# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Use a synchronized block (not method) to safely increment a shared counter using multiple threads.


## AIM:

To use a synchronized block (not method) to safely increment a shared counter using multiple threads.


## ALGORITHM :
Start the program.

Read from the user:

Number of threads (NUM_THREADS)

Number of increments per thread (INCREMENTS_PER_THREAD)

Create a shared counter (counter) and a shared lock object.

Create the specified number of threads.

Each thread:

Runs a loop for INCREMENTS_PER_THREAD times.

Uses a synchronized block to safely increment the shared counter.

Start all threads.

Wait for all threads to finish using join().

Display the final value of the shared counter.

End the program.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.util.ArrayList;
import java.util.List;

public class SynchronizedCounter {
    // Shared object to be locked
    private static final Object lock = new Object();
    
    // Shared resource (the counter)
    private static long counter = 0; 
    
    // Total number of threads and increments per thread read from input
    private static int NUM_THREADS; 
    private static int INCREMENTS_PER_THREAD; 

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        try {
            // Read NUM_THREADS (e.g., 8)
            NUM_THREADS = scanner.nextInt(); 
            // Read INCREMENTS_PER_THREAD (e.g., 800)
            INCREMENTS_PER_THREAD = scanner.nextInt();
        } catch (Exception e) {
            // Handle case where input is invalid or missing
            return;
        } finally {
            scanner.close();
        }

        List<Thread> threads = new ArrayList<>();
        
        // Create and start the specified number of threads
        for (int i = 0; i < NUM_THREADS; i++) {
            Thread t = new Thread(new CounterTask(), "Thread-" + i);
            threads.add(t);
            t.start();
        }

        // Wait for all threads to complete their execution (join)
        for (Thread t : threads) {
            try {
                t.join();
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        }

        // Calculate expected final count for verification
        long expectedCount = (long) NUM_THREADS * INCREMENTS_PER_THREAD;
        
        // Print the final result
        System.out.println("Final count: " + counter);
        
        // Optional: Verification print
        // System.out.println("Expected count: " + expectedCount);
    }

    static class CounterTask implements Runnable {
        @Override
        public void run() {
            for (int i = 0; i < INCREMENTS_PER_THREAD; i++) {
                // Use a synchronized block to protect the shared 'counter' variable
                synchronized (lock) {
                    counter++;
                }
            }
        }
    }
}
```





## OUTPUT:
<img width="562" height="319" alt="image" src="https://github.com/user-attachments/assets/63255c90-7c41-45ee-9469-b4b2e87d9e66" />



## RESULT:
The program successfully increments the shared counter using multiple threads.
Each increment is safely synchronized, preventing race conditions.
The final count matches the expected value:
Final count = NUM_THREADS × INCREMENTS_PER_THREAD
