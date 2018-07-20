# Square-1

## Background

Rather than using an existing tutorial or guide for the Square-1, I wanted to figure out a method / solution by myself. This document describes the approach and algorithms that I came up with through intuition, experimentation and perseverance!

This is **not** a guide or tutorial and it is only intended for people who are already familiar with the Square-1.

My Square-1 method has undergone a number of refinements since it's inception and I've described all of the incremental improvements in this document.

For the sake of clarity, pre-existing Square-1 terminology will be used to describe my method / solution.




## My Approach

I came up with the following steps which are essentially the same as the "Vandenbergh" method:

1. Cube Shape
2. Corner Separation (AKA Corner Orientation )
3. Edge Separation (AKA Edge Orientation)
4. Corner Permutation
5. Edge Permutation (includes Parity Fix)
6. E-Slice



## Cube Shape

I initially used intuition and trial / error but I eventually discovered that grouping all 8 edges was the easiest approach. Grouping the 8 edges then working through various shapes provided a reliable solution:

- Scallop / Scallop using /
- Barrel / Barrel using (2,4) /
- Kite / Kite using (1,2) /
- Square / Square using (-3,-3) /

The only tricky case using this cases is when 6 edges are grouped and the remaining 2 edges form and L. In this instance two edges need to be broken off from the 6 and the 2 edges in the L need to be split up.



## Corner Orientation

This step is very intuitive and is similar to L2C (Last 2 Centres) during a 4x4x4 solve.

It typically starts with a (1,0) or (0,-1) and is followed by twists and turns such as (3,0), (0,-3), (-3,3), etc.

I don't see any point in writing it up in any more detail within this document.



## Edge Orientation

Ever since v2.2 my primary algorithm for edge orientation has been a **pure swap** of **UB+UR** with **DB+DR**:

(-2,0) / (-3,0) / (-1,-1) / (4,1) / [2,0]

I really like the pure effect of this algorithm and how it can be used to solve any edge orientation.



My secondary algorithm for edge orientation since v1.0 has been a **pure swap** of **UF+UB** with **DB+DF**:

(1,0) / (-1,-1) / [0,1]

Note how this algorithm behaves much the same as **M2** does on a 3x3x3.



v2.3 introduced a tertiary algorithm equivalent of swapping **UR** with **DR** but also affecting the permutation of the U and D layers:

(1,0) / (-3,0) / (-3,0) / (-1,-1) / (1,-2) / (-3,0) / [2,6]

This algorithm was initially discovered with a different pre-AUF:

(-2,0) / (-3,0) / (-3,0) / (-1,-1) / (1,-2) / (-3,0) / [-1,0]

Note that neither of these algorithms are move optimal as a 5-twist algorithm exists in other guides.



### Redundant Algorithms

v2.2 had a primary algorithm which swapped **UB+UR** with **DB+DR** whilst preserving everything else:

(-2,0) / (-4,-1) / (1,1) / (3,0) / [2,0]

Note that this is a **pure swap** of two pairs of adjacent edges and is the inverse of the v2.5 algorithm.



v2.1 had a primary algorithm which swapped **UB+UR** with **DB+DR** but it also affected the permutation:

(-2,0) / (-4,-1) / (-2,-2) / (-3,0) / [-4,6]

Note that this is just a modified version of the v2.0 algorithm.



v2.0 had a primary algorithm which swapped **UL+UB** with **DB+DR** but it also affected the permutation:

(1,0) / (-4,-1) / (-2,-2) / (-3,0) / [5,6]

Note that this this was my first algorithm which actually stayed in cube shape.



v1.0 had a primary algorithm which swapped **UL+UF** with **DF+DR** but it also affected the permutation:

(1,0) / (-1,0) / (-3,3) / (3,-3) / (-2,3) / [-1,0]

Note that this algorithm leaves cube shape and switches to **Kite / Kite**.



## Corner Permutation

Ever since v2.4 my primary algorithm for CP has been a **J-Perm / J-Perm** which swaps **UFL-UFR** and **DFL-DFR**:

/ (-3,0) / (3,3) / (0,-3) /

Note that this algorithm leaves cube shape and switches to **Kite / Kite** and **Fist / Fist**.



My secondary algorithm for CP since v1.0 has been an **N-Perm / N-Perm** which can be used for a **diagonal** corner swap of the **U** and **D** layers:

/ (-3,3) / (3,-3) /

Note how this algorithm leaves cube shape (switches to **Kite/ Kite**) and it flips the **E-Slice**.



A slightly longer **N-Perm / N-Perm** algorithm for a **diagonal** corner swap of the **U** and **D** layers that does not affect the **E-slice** was also discovered:

/ (3,3) / (6,0) / (-3,-3) /

Note how this algorithm leaves cube shape (switches to **Kite / Kite**).



### Redundant Algorithms

v2.1 had a primary algorithm of **J-Perm / J-Perm** which swapped **UFL-UFR** and **DFL-DFR**:

(1,0) / (-3,0) / (-3,-3) / (-3,0) / [5,6]

Note that this retains the cube shape and is just a modified version of the v2.0 algorithm.



v2.0 had a primary algorithm of **J-Perm / J-Perm** which swapped **UBL-UBR** and **DBL-DBR**:

(1,0) / (3,0) / (3,3) / (3,0) / [5,6]

Note that this this was my first **J-Perm / J-Perm** algorithm which actually stayed in cube shape.



v2.0 had a secondary algorithm of **N-Perm / N-Perm **used for a **diagonal** corner swap of the **U** and **D** layer:

(1,0) / (3,3) / (6,0) / (-3,-3) / [-1,0]

Note that this this was my first **N-Perm / N-Perm** algorithm which actually stayed in cube shape.



v1.0 had a primary algorithm of **J-Perm / J-Perm** which swapped **UBL-UBR** and **DBR-DFR**:

/ (3,3) / (-3,0) / (3,0) / (-3,-3) /

Note that this algorithm leaves cube shape and switches to **Kite / Kite** and **Barrel / Barrel**.



## Edge Permutation

Ever since v2.1 my primary algorithm for EP has been an **Adj / Adj** swap of **UB-UR** and **DB-DR**:

(-2,0) / (3,0) / (-1,-1) / (-2,1) / [2,0]

This algorithm can be used to concurrently solve any combinations of EP cases on the U and D layers. It is the inverse of the "redundant" v2.0 algorithm (see below).



My secondary algorithm for EP since v1.1 has been an **Opp / Opp** swap of **UF-UB** and **DF-DB**:

(1,0) / (-1,-1) / [6,0] / (1,1) / [5,0]

Note how this algorithm is essentially a cancellation of the M2 EO algorithm - **M2 U2 M2 U2**.



### Redundant Algorithms

v2.0 had a primary algorithm for the **Adj / Adj** swap of **UL-UB** and **DB-DR**:

(1,0) / (2,-1) / (1,1) / (-3,0) / [-1,0]

Prior to v2.1 the pre-AUF was changed to create an **Adj / Adj** swap of **UB-UR** and **DB-DR**:

(-2,0) / (2,-1) / (1,1) / (-3,0) / [2,0]



v1.0 had a long algorithm for performing a **U-Perm** / **U-Perm** which cycled **UB-UR-UL** and **DB-DR-DF**:

/ (3,3) / (-3,0) / (3,0) / (-3,-3) / (1,-1) / (3,3) / (-3,0) / (3,0) / (-3,-3) / [-1,1]

Note how it is simply two different J-Perm algorithms where the second is a conjugation of the first.



Note: Solving both layers simultaneously using the U-Perm / U-Perm algorithm was often quite tricky and required some careful thought. It is far more difficult complicated than swapping adjacent pairs on both layers but I didn't have such an algorithm at the time. However it did allow me to solve the Square-1!

Important: The U-Perm approach only works when there are an odd number of pair swaps in both layers. Initially I worked around this by switching two edges between the bottom and top layers using an EO algorithm, applying a J-Perm / U-Perm and re-doing the EO and CP. In v1.1 of the method, I replaced this crude approach with the **M2 U2 M2** pair swap (i.e. swapping UF-UB and DF-DB). After swapping exactly two edges on each layer the EP became solvable using the U-Perm / U-Perm approach.



## Parity

Parity occurs in 50% of solves so to begin with I just used to re-scramble the puzzle and hope for the best!

In v1.2, I started using a slightly better approach. Parity can be solved intuitively by leaving cube shape, going back to Scallop / Scallop, exchanging 3 corners and restoring cube shape:

- Kite / Kite using /
- Barrel / Barrel using (3,3) /
- Scallop / Scallop using (-1,-2) /
- Parity Fix using (-2,2) /
- Barrel / Barrel using (2,-2) /
- Kite / Kite using (1,2) /
- Square / Square using (-3,-3) /

The intuitive approach goes all the way back to corner orientation but it is guaranteed to fix parity!



## E-Slice

Flipping the E-slice is really easy and the algorithm that I found is in common use:

/ (6,0) / (6,0) / [6,0]

If the U and D layers were accidentally exchanged, I'd use the following algorithm as a quick fix:

/ (6,6) / [-1,1]



## Version History

| Version | Date       | Comment                                                      |
| ------- | ---------- | ------------------------------------------------------------ |
| v1.0    | 2018-07-04 | Established crude method allowing me to solve the Square-1   |
| v1.1    | 2018-07-06 | Utilised M2 U2 M2 for odd numbers of edge swaps during EP    |
| v1.2    | 2018-07-08 | Intuitive parity fix to avoid re-scrambling and hoping for the best! |
| v2.0    | 2018-07-09 | New algorithms to retain cube shape during CP and EP         |
| v2.1    | 2018-07-10 | Tweaked the pre-AUF for EO, CP and EP algorithms             |
| v2.2    | 2018-07-11 | Discovered a pure swap of adjacent edges for EO              |
| v2.3    | 2018-07-12 | Discovered a single edge swap for EO                         |
| v2.4    | 2018-07-13 | Returned to CP algorithms which get out of cube shape        |
| v2.5    | 2018-07-16 | Tweaked the pure swap of adjacent edges for EO               |



# References

After coming up with my own method, I've had a quick look at a few resources for Square-1.

These resources have improved my understanding and exposed me to the standard terminology.

### Guides

[How to Solve a Square-1](http://brandonlin.com/cubing/sq1tutorial.html) by Brandon Lin

[Square-1 Tutorial](http://andrewknelson.com/square-1-tutorial/) by Andrew K. Nelson

[(Back to) Square One / Cube 21](https://www.jaapsch.net/puzzles/square1.htm) on Jaap's Puzzle Page

[Square-1 Solution](http://www.cubezone.be/square1.html) on Lars Vandenbergh's CubeZone

### Links

[The "Square-1 Help / Alg Sharing" thread](https://www.speedsolving.com/forum/threads/the-square-1-help-alg-sharing-thread.37858/) on Speedsolving.com

