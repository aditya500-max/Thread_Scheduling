# Thread_Scheduling
Analysed time variations in different Scheduling policies using pthread_schedsetparam()

This exercise is to show you how to use Linux’s scheduling policies for three
threads. You need to launch three threads, each of which relies on three different
functions, countA(), countB() and countC(). Each function does the same
thing, i.e. counts from 1 – 232. The following should be the detailed specification
of each of the threads, to being with:
1. Thread 1 (call it Thr-A()): Uses SCHED OTHER scheduling discipline
with standard priority (nice:0).
2. Thread 2 (call it Thr-B()): Uses SCHED RR scheduling discipline with
default priority.
3. Thread 3 (call it Thr-C()): Uses SCHED FIFO scheduling discipline with
default priority.
Each of these threads must time the process of counting from 1 – 232. You
can use the clock gettime() function for obtaining the actual time ticks that
can be used to compute how long it took to complete a function.

We require you benchmark these three schedulers by change the schedul-
ing priorities of the three threads (keeping the scheduling priorities the same),

against the counting program.
For these cases, you would require to rely on pthread schedsetparam() and

related functions for the same. You would require to generate histograms show-
ing which scheduler completes the task when, depending upon the scheduling

policy. You may choose different colors for the histogram bars, with one axis
showing the time to complete, and the other showing the thread priorities. Of
course, you cannot plot for all possible values of priorities; you would require to
choose only some.
