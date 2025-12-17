[//]: # (Source: https://www.jetbrains.com/help/idea/detect-concurrency-issues.html)
[//]: # (Downloaded: 2025-12-17 19:24:44)

## Problem

A common example of a concurrency-related bug is a race condition. It happens when shared data is modified by several threads at the same time without being properly synchronized. Such code may work fine as long as reads and writes in the two threads don't overlap.

![Thread 1 had finished writing by the time reading in thread 2 started](https://resources.jetbrains.com/help/img/idea/2025.3/debug_concurrency_issues_tutorial_1.png)

The overlapping may be very rare and lead us into thinking there is no flaw in the code. However, when the thread operations do overlap, the data gets corrupted.

![Thread 1 hadn't started writing by the time thread 2 read the value](https://resources.jetbrains.com/help/img/idea/2025.3/debug_concurrency_issues_tutorial_2.png)

If we don't take this into account, there is no guarantee that the threads will not operate on the data simultaneously, especially if we deal with something more complex than just a single read and write. Luckily, Java has built-in synchronization mechanisms that ensure only one thread works with the data at a time.

Let's consider the following code:

import java.util.*; public class ConcurrencyTest { static final List a = Collections.synchronizedList(new ArrayList()); public static void main(String[] args) throws InterruptedException { Thread t = new Thread(() -> addIfAbsent(17)); t.start(); addIfAbsent(17); t.join(); System.out.println(a); } private static void addIfAbsent(int x) { if (!a.contains(x)) { a.add(x); } } } 

The `addIfAbsent` method checks if a list contains a specific element, and if not, adds it. We call this method twice from different threads. Both times we pass the same integer value (`17`), and because of the guard condition `(!a.contains(x))`, only the first thread to call that method should be able to add the value. The use of `SynchronizedList` is supposed to protect us against race conditions. Finally, the `System.out.println(a)` statement prints out the contents of the list.

If we were to use this code for a long time, we would see that at times it still produces unexpected results.

If you are curious and want to reproduce the unexpected behavior, you can create a test that would run over and over until the first failure.

To find the cause, let's examine how the code operates and see if we really managed to prevent race conditions.
