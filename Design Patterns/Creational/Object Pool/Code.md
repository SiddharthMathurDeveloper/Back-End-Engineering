
## Question
Design an object pool for managing database connections in a multi-threaded application. Explain the key components, their interactions, and how you would handle object creation, acquisition, and release in a thread-safe manner. Additionally, discuss any potential challenges and optimizations you would consider while implementing this object pool.
## UML :



## Code :

### Client.java
```java
public class Client {
    public static void main(String[] args) {
        int poolSize = 5; // Specify the desired pool size

        // Create an instance of the ThreadPool with the specified pool size
        ThreadPool threadPool = new ThreadPool(poolSize);

        // Use threads from the pool
        for (int i = 0; i < 10; i++) {
            try {
                Thread thread = threadPool.getThread();

                // Perform some work with the acquired thread
                // For simplicity, we'll just sleep for a while here
                System.out.println("Working with thread: " + thread.getId());
                Thread.sleep(1000); // Simulate some work

                // Release the thread back to the pool
                threadPool.releaseThread(thread);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }

        // Optionally, you can shut down the thread pool when done
        threadPool.shutdown();
    }
}
```


### Poolable.java
```java
public interface Poolable {
    void releaseThread(Thread thread); //// Reset the state of the object when returning it to the pool
} 
```


### ThreadPool.java
```java
public class ThreadPool implements  Poolable {
    private BlockingQueue<Thread> threadPool;

    public ThreadPool(int poolSize) {
        threadPool = new ArrayBlockingQueue<>(poolSize);

        // Initialize the pool with threads
        for (int i = 0; i < poolSize; i++) {
            Thread thread = new Thread();
            threadPool.offer(thread);
        }
    }

    public Thread getThread() throws InterruptedException {
        return threadPool.take(); // Take a thread from the pool
    }


    public void shutdown() {
        // Optionally, you can add logic here to gracefully shut down threads
    }

    @Override
    public void releaseThread(Thread thread) {
        if (thread != null) {
            threadPool.offer(thread); // Return the thread to the pool

        }
    }

    @Override
    public String toString() {
        return "ThreadPool{" +
                "threadPool=" + threadPool +
                '}';
    }
}
```












