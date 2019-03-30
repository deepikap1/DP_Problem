# DP_Problem
The Dining Philosopher Problem – 
The Dining Philosopher Problem states that K philosophers seated around a circular table with one chopstick between each pair of philosophers. There is one chopstick between each philosopher. A philosopher may eat if he can pickup the two chopsticks adjacent to him. One chopstick may be picked up by any one of its adjacent followers but not both.
# Semaphore Solution to Dining Philosopher –
Each philosopher is represented by the following pseudocode:

1.process P[i]
2.while true do
3.{  THINK;
4.    PICKUP(CHOPSTICK[i], CHOPSTICK[i+1 mod 5]);
5.    EAT;
6.   PUTDOWN(CHOPSTICK[i], CHOPSTICK[i+1 mod 5])
   }
There are three states of philosopher: THINKING, HUNGRY and EATING. 
Here there are two semaphores: Mutex and a semaphore array for the philosophers. The mutex is used such that no two philosophers may access the pickup or putdown at the same time. The array is used to control the behaviour of each philosopher.
