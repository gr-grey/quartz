---
title: "Traveling salesman problem"
date: "2023-08-09"
tags:
- ramblings
---

You are a traveling salesman.
You have a bunch of cities to visit and make sales.
Your want to come up with a traveling route, that covers *every single city*, and visit each city *exactly once*, and come back to the city you started with.
What is the shortest route possible?

![[attachments/traveling-sales-man.png]]
Here is one possible route that goes through every city (black dots) and ends up in the beginning one. The beginning one is marked with the blue circle, but since this is a closed up loop, you could start with any dot on the path.

This is a simple problem, but hard, because of the combinatorial nature.
It's NP-hard, like the protein folding problem.

It turns out *ants* already know how to solve this problem through swarm/ group intelligence. 

Ants have a colony/ home, which is the starting city, and the city they'll come back to.
The other cities are attracting food places.
You are an ant lord, and you want to establish a shortest path of foraging, so each one of your working ants spend the least amount of energy when they go through each food location to take food back home.

This is how ants solve the problem.

They send out two batches of ants.
The first batch of ants start from each city and mark paths between cities with their pheromones - they leave a trail of pheromones as they travel.

Two simple rules with pheromone:
1. Each ant has a limited amount of total pheromones.
2. The pheromones dries out overtime.

These two rules are the selective force that drives ants to find more optimal (shorter) connections between the cities. 
The optimization result: the shorter the distance, the thicker the pheromone trail.
The first batch of ants explore and gather initial information about different parts of the solution space.

The second batch of ants are sent out, and wander around randomly with their own little bags of pheromone, until they hit a trail of existing pheromones, then they may join the path and lay down their own pheromones to strengthen the signal.
The thicker the trail, the more likely an ant would join it.

Have enough of ants, and they'll draw out the thickest pheromones, and solve the traveling sales man problem for you.

P.S.
Completely unrelated, I walked to my office this morning (walking for 30 min around 2pm yesterday gave me a sunburn, thanks Texas 😒), and saw some early morning dew thingy on grasses. They sparkle like little specks of diamonds, it was beautiful ✨.