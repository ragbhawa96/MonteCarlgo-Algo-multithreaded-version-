Calculate π using Monte Carlo algorithm

This is a multithreaded version of this algorithm, where you create several threads (at
least two excluding the main thread), each of which generates random points (for an
example 100 points) and determines if the points fall within the circle. Each thread will
have to update two global variables, the number of points in the circle and the total
number of points. While child threads are generating random points and updating the
global variables, the main thread continuously calculates the value of pi and display it on
the console. Main thread finishes the calculation when all child threads exited.

You can do xperiments with the number of points generated by a thread and the number of threads.
As a general rule, the greater the number of points, the closer the approximation to pi.

This program protects against race conditions on updates to the shared global variables
by using mutex locks.