---
layout: post
title: Proof of Work based off of Rubik's Cubes
---

**Disclaimer: This PoW method might not be necessarily better but it is definitely another proof of work method lmao.**

Hello everyone, I had a lot of free time on my hands as 11th grade comes to a close. I was always obsessed with how proof of work could somehow create this sort of "consensus" among a large user base and I was trying to invent different new proof of work methods that were weird and unique that may turn out to be viable. I realized that rubiks cubes might work in creating a PoW that would be hard and scalable as if we ran out of different combinations for the base 3x3 rubik's cube we can easily increase the difficulty and add more possibilities. ***(will talk about this later in the post)***. 

**So here's my proposed proof of work.** 

> There are **43,000,000,000,000,000,000** possible states on a 3x3 rubik's cube and exponentially more for higher nxn. 

The goal of this proof of work is to show the transition (or exact sequence of moves) between one state and another state composed in rubik's cube notation **(https://ruwix.com/the-rubiks-cube/notation/)**. Finding this is hard and I do not know at the moment ***(maybe im ignorant)*** if there is a proposed algorithm for this.

The resulting sequences of moves that would show how you transitioned from one rubiks cube state to another would be the PoW you would show to the chain to validate the block. If we ever run out of scrambles we have the possibility of scaling up. For example, if we run out of all the 43 quintillion states that the 3x3 rubik's cube has we can easily upgrade to the 4x4 rubik's cube and so on for any nxn. Computers can easily simulate an nxn rubik's cube. Making a program that outputs the sequences of moves to one state to the next will be really difficult as you get to higher nxn cubes. 

>A funny thought experiment for this proof of work is that you can imagine a "pool" of workers trying to "mine" the solution by twisting and turning the cubes arbitrarily and it made me laugh hysterically thinking about it. 

Anyhow, this blog post is just me toying around and having fun in my free time with weird abstractions and ideas. Hope you guys enjoyed this post I hope people dont take this super seriously as I dont know if this can be implemented wide scale. I might actually make a cryptocurrency with this proof of work mechanism so stay tuned!

Thanks for reading. 
  - Aditya 


> Follow my github!: https://github.com/SriLikesToSing









