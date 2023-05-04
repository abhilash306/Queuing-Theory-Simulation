# Queuing-Theory-Simulation

# Problem 1
Generate Poisson distributed random packet arrival process with arrival rate λ= 
5 packets per second from the first principles (i.e., using basic uniformly 
distributed RAND function between 0and 1). Find the distribution (pdf) of 
packet inter-arrival times and plot it.
# Problem 2
Consider an M/M/1 queueing system with arrival rate λ= 5 packets per second 
and service rate μ= 7 packets per second. 
(a) Plot the probability of n packets in the system, where n varies from 0 to ∞. 
(b) Repeat the exercise in (a), with μ= 4 packets per second, and comment on 
the two results.
# Implementation 1st Problem
- Inter-arrival time is the time between the successful arrival of two different 
packets. For a poisson distributed random packets, inter-arrival time is 
exponentially distributed. 
- Arrival rate (λ) is given as 5 packets per sec. 
- The time between two successive arrival is calculated and pdf of thus achieved 
inter-arrival time is calculated. 
# Implementation 2nd Problem
- MATLAB simulation is performed to solve the above problem. 
-λ denote arrival rate and μ denote the departure rate, where both arrivals and 
departures are treated as exponential processes. That is, if there are currently n 
customers, the time until the next event is an exponential random variable with 
rate λ + μ; the probability that the next event is an arrival is 
-We assume the queue is initially empty, so generate a first arrival to the queue 
with rate λ 
-The next event can be either an arrival or departure. The time T1 until that next 
event is an exponential random variable with rate λ + μ. 
-To determine whether that event is an arrival or a departure, generate an array 
of random number of length approximately to integer value equal to T1(interval 
of time generated from exponential random number) having p between 0 and 1. 
- Running loop till integer value equal to T1(interval of time generated from 
exponential random number). If p < , then the event is an arrival, 
otherwise it’s a departure. If its arrival we calculate the number of packets in the 
time interval T1 in count1 and if its departure then we calculate number packets 
that departed in count2. 
- We store each count values for each iteration in array strcount for both arrived 
and departed packets and also store the probability for each iteration by 
calculating number of packets arrived by total number of packets was in the 
system in each iteration
