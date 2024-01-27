---
layout: project
type: project
image: 
title: "Queue Simulator"
date: 2023
published: true
labels:
  - Java
  - Simulation
summary: "A small coding project I made for ICS 211."
---
Queue Simulator is a small project I made to simulate the difference between a single customer queue feeding into multiple servers and multiple customer queues, where each queue leads into a single server. 

This was meant to be a highly reductive model of two different ways to set up a grocery store in order to prove that, on average, each customer of a single queue setup will wait less time than each customer of a multiqueue setup.

The program consists of a Customer class, with pseudorandom arrival and service times, and a Server class, which tracks whether a new Customer can be served or not and, for some reason, also contains the method to run a simulation. Looking back now, it does not make much sense. But hey, that means I'm learning!

Here's a snippet from the multiqueue simulation:
```
for (int i = 0; i < queues.length; i++) {
				queues[i] = new LinkedList<Customer>();
			}

			for (int second = 0; second < 86400; second++) {

				// Find smallest queue
				int smallestQueueIndex = 0;
				for (int i = 0; i < queues.length; i++) {
					if (queues[i].size() < queues[smallestQueueIndex].size()) {
						smallestQueueIndex = i;
					}
				}
				// Add arriving customers to the queue
				while (!allCustomers.isEmpty() && customerArrived(allCustomers.peek(), second)) {
					queues[smallestQueueIndex].offer(allCustomers.poll());
				}

				// Servers serve the next customer if idle
				for (int i = 0; i < servers.length; i++) {
					Server server = servers[i];
					if (!queues[i].isEmpty() && server.isIdle(second)) {
						server.serve(queues[i].poll(), second);
					}
				}

				for (int i = 0; i < servers.length; i++) {
					totalWaitingTime += queues[i].size();
				}
			}
```
It is not very optimized, but at that point I had only just begun dipping my toes into big O's. Y'know?

Anyway, the simulation itself had pretty interesting results - specifically, that a single customer queue feeding into several servers is faster on average than a queue for each server. That is, assuming customers are instantly served the moment a server is available, customers perfectly choose the shortest queue, servers all work at the same speed, no problems occur... you get the gist.

Still, it was fun to get to work with a tick system of sorts, since they are in many real-time applications like video games. I liked coming up with the checks needed at every simulated second and, if I were to revisit this or start something similar, I think it would be fun trying to squeeze performance out of those checks.
