---
layout: post
title: Computational Complexity Rabbit Hole
---

These are the notes (Not finished yet) I have taken while spiralling down the rabbit hole of computational complexity theory. It is just so vast and is such a beautiful field in theoretical computer science.



What type of computational problems are there?

 - Problems that take an infinite amount of time
    - Can a different computation scheme help solve problems in this category?
        - Quantum Computing
    - Halting problem
        - Given an infinite amount of programs can you tell if every single one of them will halt at some point?

 - Problems that take a finite amount of time
    - There are problems that can be solved in polynomial time (P)
         - Given a decision problem with yes or no, you can write a program that can output yes given a polynomial time
                O(n^k): n -> input size: k -> some arbitrary constant

                - Since you can find a solution in polynomial time that also means your basically checking it in polynomial time so P is inside of
                    NP (Non Deterministic)

         - The class that contains P is called NP (Non Deterministic)
             - Any decision problem (not sure what other types) that is in NP can be checkedin Polynomial time
                - most computational problems can be watered down to decision problems
             - A non deterministic Turing Machine can solve it in polynomial time
                 - A non deterministic turing machine basically uses a lucky algorithm
                     - It guesses and it will basically always guess right in polynomial time



- Why doesent P = EXPTIME?:
    - If we can prove that there exist problems that cannot be optimized into O(n^k) then we can say that EXP != P because if EXP = P then
        all EXP problems should be in P.
            - Time Hierarchy theorem:
                - for any reasonable function f there are problems which can be decided in O(f(n)) that cannot be decided in O(f(n)/n)
                    - If thats the case, then there are problems that can be solved in time O(2^n) that cannot be solved in time O(2^n/n)

                - every EXPTIME COMPLETE problem is not in P according to Time hierarchy theorem

    - Why can we prove that P != EXPTIME but we cant prove P != NP or NP != EXPTIME?
        - TRYING TO SOLVE RIGHT NOW

