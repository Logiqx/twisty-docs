# Square-1

## Background

This is a list of Square-1 algorithms from a number of decent resources for beginners / intermediates.

This is **not** a guide or tutorial and it is only intended for people who are already familiar with the Square-1.

The resources are listed at the end of this document.



## Cube Shape

| Source  | Starting Position          | Algorithm                 |
| ------- | -------------------------- | ------------------------- |
| Brandon | 8 connected edges at back  | / -4,-2 / 2,1 / 3,3 /     |
| DGCubes | 8 connected edges at front | / -2,-4 / -1,-2 / -3,-3 / |
| Noob    | 8 connected edges at back  | / 2,4 / 1,2 / -3,-3 /     |

Useful links for cube shapes:

- [Square-1 Shape](http://hem.bredband.net/_zlv_/rubiks/sq1/sq1-shape-depth.html) by Stefan Lidstrom

- [Square-1 Full Cubeshape](http://andrewknelson.com/2012/03/23/square-1-full-cubeshape/) by Andrew K. Nelson

- [Square-1 Shapes](https://www.jaapsch.net/puzzles/square1d.htm) by Jaap - nice graph view!




## Corner Orientation

I don't see any point in writing up CO algorithms in any detail.



## Edge Orientation

### Adjacent / Adjacent

| Source                         | Effect                    | Algorithm                          |
| ------------------------------ | ------------------------- | ---------------------------------- |
| Brandon<br />Andrew<br />Sarah | Swap UL-DF and UF-DR      | 1,0 / 3,0 / -1,-1 / -3,0 / [0,1] * |
| Lars                           | Pure swap UL-DR and UB-DF | 1,0 / -3,0 / -1,-1 / 4,1 / [-1,0]  |
| Noob                           | Pure swap UB-DB and UR-DR | -2,0 / -3,0 / -1,-1 / 4,1 / [2,0]  |

### Opposite / Opposite

| Source                                   | Effect                    | Algorithm             |
| ---------------------------------------- | ------------------------- | --------------------- |
| Brandon<br />Andrew<br />Sarah<br />Noob | Pure swap UF-DB and UB-DF | 1,0 / -1,-1 / [0,1] * |
| Lars<br />Andrew                         | Pure swap UF-DB and UB-DF | 0,-1 / 1,1 / [-1,0]   |

### Single / Single

| Source             | Effect     | Algorithm                                        |
| ------------------ | ---------- | ------------------------------------------------ |
| Brandon<br />Sarah | Swap UR-DB | 1,0 / 3,0 / 3,0 / -1,-1 / -2,1 / -3,0 / [-1,0] * |
| DGCubes            | Swap UR-DR | 1,0 / 0,-3 / 0,-3 / -1,-1 / 1,4 / 0,3 / [-1,0]   |
| Andrew<br />Lars   | Swap UB-DF | 0,-1 / -3,0 / 4,1 / -4,-1 / 3,0 / [0,1]          |
| Noob               | Swap UR-DR | 1,0 / -3,0 / -3,0 / -1,-1 / 1,-2 / -3,0 / [2,6]  |

### 3 Edges

| Source              | Effect                     | Algorithm                                       |
| ------------------- | -------------------------- | ----------------------------------------------- |
| Brandon<br />Andrew | Swap UL-UF-UR and DF-DR-DB | 1,0 / 3,0 / 3,0 / -1,-1 / -3,0 / -3,0 / [0,1] * |
| Sarah               | Swap UF-UR-UB and DF-DR-DB | 0,-1 / 3,0 / 3,0 / 1,1 / -3,0 / -3,0 / [-1,0]   |
| Noob                | Swap UF-UR-UB and DF-DR-DB | 1,0 / -3,0 / -3,0 / -1,-1 / 3,0 / 3,0 / [0,1]   |

### 4 Edges

| Source                   | Effect      | Algorithm                           |
| ------------------------ | ----------- | ----------------------------------- |
| Brandon                  | All 4 edges | 1,0 / -1,-1 / -3,3 / 1,1 / [-1,0] * |
| Brandon (original video) | All 4 edges | 1,0 / -1,-1 / -2,4 / -1,-1 / [0,1]  |
| Sarah                    | All 4 edges | 1,0 / -1,-1 / 3,3 / 1,1 / [-1,0]    |
| Noob                     | All 4 edges | 1,0 / -1,-1 / -2,-2 / -1,-1 / [0,1] |

### Adj / Opp

| Source             | Effect               | Algorithm                                        |
| ------------------ | -------------------- | ------------------------------------------------ |
| Brandon<br />Sarah | Swap UL-UB and DF-DB | 1,0 / 3,0 / 3,0 / -1,-1 / -2,1 / -4,-1 / [0,1] * |

### Opp / Adj

| Source  | Effect               | Algorithm                                               |
| ------- | -------------------- | ------------------------------------------------------- |
| Brandon | Swap UB-UF and DF-DR | 0,-1 / 3,0 / -3,0 / 1,1 / 3,0 / -3,0 / [-1,0] *         |
| Sarah   | Swap UB-UF and DL-DF | 0,-1 / 0,-3 / 0,-3 / 1,1 / -1,2 / 1,4 / [-1,0] - broken |



## Corner Permutation

### J / J

| Source                                  | Effect                   | Algorithm               |
| --------------------------------------- | ------------------------ | ----------------------- |
| Brandon<br />Andrew<br />Lars<br />Noob | Swap UFL-UFR and DFL-DFR | / -3,0 / 3,3 / 0,-3 / * |
| Sarah                                   | Swap UBL-UBR and DBL-DBR | / 3,0 / -3,-3 / 0,3 /   |

### N / N

| Source                         | Effect                | Algorithm         |
| ------------------------------ | --------------------- | ----------------- |
| Brandon<br />Andrew<br />Sarah | Swap diagonal corners | / 3,-3 / -3,3 / * |
| Lars                           | Swap diagonal corners | / 3,-3 / 3,-3 /   |
| Noob                           | Swap diagonal corners | / -3,3 / 3,-3 /   |

### N / J

| Source            | Effect       | Algorithm                     |
| ----------------- | ------------ | ----------------------------- |
| Brandon           | Swap DFR-DBR | / -3,0 / 3,0 / -3,0 / 3,0 / * |
| Andrew<br />Sarah | Swap DFR-DBR | / 3,0 / -3,0 / 3,0 / -3,0 /   |

### J / N

| Source  | Effect       | Algorithm                     |
| ------- | ------------ | ----------------------------- |
| Brandon | Swap UFR-UBR | / 0,-3 / 0,3 / 0,-3 / 0,3 / * |
| Sarah   | Swap UFR-UBR | / 0,3 / 0,-3 / 0,3 / 0,-3 /   |

### Solved / J

| Source                       | Effect       | Algorithm                          |
| ---------------------------- | ------------ | ---------------------------------- |
| Brandon<br />Lars<br />Sarah | Swap DFL-DFR | / 3,-3 / 0,3 / -3,0 / 3,0 / -3,0 / |
| DGCubes                      | Swap DFL-DFR | / 3,-3 / -3,0 / 0,3 / 0,-3 / 0,3 / |

### J / Solved

| Source  | Effect       | Algorithm                          |
| ------- | ------------ | ---------------------------------- |
| Brandon | Swap UFL-UFR | / 3,-3 / 3,0 / -3,0 / 0,3 / -3,0 / |
| Andrew  | Swap UFR-UBR | / 3,0 / -3,0 / -3,3 / -3,0 / 3,0 / |
| Sarah   | Swap UFL-UFR | / 3,-3 / -3,0 / 0,3 / 0,-3 / 0,3 / |

### Solved / N

| Source  | Effect | Algorithm                               |
| ------- | ------ | --------------------------------------- |
| Brandon |        | / -3,-3 / 0,3 / -3,-3 / 0,3 / -3,-3 /   |
| Sarah   |        | / -3,-3 / 0,-3 / -3,-3 / 0,-3 / -3,-3 / |

### N / Solved

| Source            | Effect | Algorithm                               |
| ----------------- | ------ | --------------------------------------- |
| Brandon           |        | / -3,-3 / -3,0 / -3,-3 / -3,0 / -3,-3 / |
| Andrew<br />Sarah |        | / -3,-3 / 3,0 / -3,-3 / 3,0 / -3,-3 /   |



## Edge Permutation

There are 99 algorithms in total but 16 cover 44.4% of solves by combining these cases:

- Adjacent
- CW U
- CCW U
- O

Note: Charlie's spreadsheet shows the probabilities and combinations of the above are 256/576 or 44.4%.

### Adjacent / Adjacent

| Source                         | Effect               | Algorithm                         |
| ------------------------------ | -------------------- | --------------------------------- |
| Brandon<br />DGCubes<br />Noob | Swap UB-UR and DB-DR | -2,0 / 3,0 / -1,-1 / -2,1 / [2,0] |
| Andrew                         | Swap UL-UF and DL-DF | 0,2 / -3,0 / 1,1 / 2,-1 / [0,-2]  |

### Opposite / Opposite

| Source  | Effect               | Algorithm                                     |
| ------- | -------------------- | --------------------------------------------- |
| Andrew  | Swap UF-UB and DF-DB | 1,0 / -1,-1 / 6,0 / 1,1 / [5,0]               |
| Brandon | Swap UF-UB and DF-DB | 1,0 / -1,-1 / 0,1 / 6,0 / 1,0 / -1,-1 / [6,1] |
| Lars    | Swap UF-UB and DF-DB | 1,0 / 5,-1 / -5,1 / [5,0]                     |
| Noob    | Swap UF-UB and DF-DB | 1,0 / -1,-1 / -5,1 / -1,-1 / [6,1]            |

### TODO

Other cases from [Brandon](https://www.youtube.com/watch?v=Gkvl1xQhTu0):

- U / U
- U / Adj and Adj / U
- Opp / Adj and Adj / Opp
- U / Solved, Z / Solved, H / Solved
- O / Opposite
- See video - [EP Algorithms Every Square-1 Solver Should Know](https://www.youtube.com/watch?v=ts9qk1zfQT8)

Other cases from [Andrew](http://andrewknelson.com/square-1-tutorial/more-edge-permutation/):

- Opp / Adj
- U / Solved, Z / Solved, H / Solved
- O / Opposite

AlgDB.net:

- Check cases listed above



## Parity

| Source                                | Effect | Algorithm                                                    |
| ------------------------------------- | ------ | ------------------------------------------------------------ |
| Brandon<br />Charlie                  | CCW O  | / 3,3 / 1,0 / -2,-2 / 2,0 / 2,2 / -1,0 / -3,-3 / 0,2 / -2,-2 / [-1,0] * |
| Brandon<br />Charlie                  | CW O   | / 3,3 / 1,0 / -2,-2 / -2,0 / 2,2 / -1,0 / -3,-3 / 1,0 / 2,2 / [-1,0] * |
| Charlie                               | UF-UB  | / 3,3 / 1,0 / -2,-2 / 2,0 / 2,2 / (0,-2 / -1,-1 / 0,3) / -3,-3 / 0,2 / -2,-2 / [-1,0] * |
| Charlie                               | UF-UB  | / -3,0 / 0,3 / 0,-3 / 0,3 / -4,0 / 0,2 / -2,0 / 4,0 / 0,-2 / 0,2 / -1,1 / -3,0 / 3,0 / [?,?] |
| Brandon (original video)<br />DGCubes | UF-UB  | / -3,0 / 0,3 / 0,-3 / 0,3 / 2,0 / 0,2 / -2,0 / 4,0 / 0,-2 / 0,2 / -1,4 / 0,-3 / [0,3] |
| Jaap                                  | UF-UB  | / 3,3 / 1,0 / -2,-2 / 2,0 / 2,2 / -1,0 / -3,-3 / -2,0 / 3,3 / 3,0 / -1,-1 / -3,0 / 1,1 / [-4,-3] |

Charlie Stark's algorithms were taken from Speedsolving.com:

- https://www.speedsolving.com/forum/threads/the-square-1-help-alg-sharing-thread.37858/page-30#post-1200039

- https://www.speedsolving.com/forum/threads/square-1-edge-parity.63931/#post-1220690




## Miscellaneous

### E-Slice

| Source                                               | Effect           | Algorithm            |
| ---------------------------------------------------- | ---------------- | -------------------- |
| Brandon<br />Andrew<br />DGCubes<br />Lars<br />Noob | Flip the equator | / 6,0 / 6 ,0 / [6,0] |

### Exchanging Layers

| Source                         | Effect           | Algorithm            |
| ------------------------------ | ---------------- | -------------------- |
| Brandon<br />DGCubes<br />Noob | Swap both layers | / 6,6 / [-1,1]       |
| Lars                           | Swap both layers | / 1,0 / 6,6 / [-1,0] |



## Version History

| Version | Date       | Comment       |
| ------- | ---------- | ------------- |
| v1.0    | 2018-07-16 | Initial draft |



# Resources

The following resources have been used to create this document.

### Videos

[How to Solve a Square-1](https://www.youtube.com/watch?v=Ds2lC5bVui4) by Brandon Lin - Aug 11, 2013

```
L-shape -＞ 8 edges: (3,-2)/(0,2)/
Edge Orientation Edge Swap: (1,0)/(3,0)/(3,0)/(-1,-1)/(-2,1)/(-3,0)/
Corner Permutation Corner Swap: /(3,-3)/(0,3)/(-3,0)/(3,0)/(-3,0)/
Swap the 2 Layers: /(6,6)/
Edge Permutation Edge Swap: (-2,0)/(3,0)/(-1,-1)/(-2,1)/(2,0)
Middle Layer Flip: /(6,0)/(6,0)/(6,0)
PARITY ALG: /(-3,0)/(0,3)/(0,-3)/(0,3)/(2,0)/(0,2)/(-2,0)/(4,0)/(0,-2)/(0,2)/(-1,4)/(0,-3)/(0,3) 
```

[How to Get Fast on Square-1](https://www.youtube.com/watch?v=Gkvl1xQhTu0) by Brandon Lin - Feb 3, 2014

```
EP algorithms start at 14:58

TODO - transcribe from video
```

[Square-1 EO and CP Algorithms](https://youtu.be/y8KOpnjC6hY) by Brandon Lin - Dec 30, 2014 

```
EO:
One-One: 1,0/3,0/3,0/-1,-1/-2,1/-3,0/
M2: 1,0/-1,-1/
L-L: 1,0/3,0/-1,-1/-3,0/
L-I: 1,0/3,0/3,0/-1,-1/-2,1/-4,-1/
I-L: 0,-1/3,0/-3,0/1,1/3,0/-3,0/
Three-Three: 1,0/3,0/3,0/-1,-1/-3,0/-3,0/
Double M2: 1,0/-1,-1/-2,4/-1,-1/

CP:
Bottom J: /3,-3/0,3/-3,0/3,0/-3,0/
Top J: /3,-3/3,0/-3,0/0,3/-3,0/
Double J: /-3,0/3,3/0,-3/
Bottom N: /-3,-3/0,3/-3,-3/0,3/-3,-3/
Top N: /-3,-3/-3,0/-3,-3/-3,0/-3,-3/
Double N: /3,-3/-3,3/
J-N: /0,-3/0,3/0,-3/0,3/
N-J: /-3,0/3,0/-3,0/3,0/
```

[EP Algorithms Every Square-1 Solver Should Know](https://www.youtube.com/watch?v=ts9qk1zfQT8) by Brandon Lin - Sep 7, 2015

```
ALGORITHMS: (Cw stands for clockwise and Ccw means counter-clockwise

Adj-Adj: -2,0/3,0/-1,-1/-2,1/ or 1,0/0,3/-1,-1/1,-2/ or 0,-1/-3,0/1,1/2,-1/

CwU-CwU: 1,0/5,-1/-3,0/1,1/-3,0/
CcwU-CcwU: 1,0/3,0/-1,-1/3,0/-5,1/

CwU: /3,0/1,0/0,-3/-1,0/-3,0/1,0/0,3/
CcwU: 1,0/0,-3/-1,0/3,0/1,0/0,3/-1,0/-3,0/

Z: M2 U' M2 U M2

H: M2 U' M2 U2 M2 U' M2

Opp-Adj: 1,0/0,-1/0,-3/5,0/-5,0/0,3/0,1/
Adj-Opp: 0,-1/1,0/3,0/6,1/5,0/-3,0/0,-1/

CwO: /3,3/1,0/-2,-2/-2,0/2,2/-1,0/-3,-3/1,0/2,2/
CcwO: /3,3/1,0/-2,-2/2,0/2,2/-1,0/-3,-3/0,2/-2,-2/

Opp: /3,3/1,0/-2,-2/2,0/2,2/0,-2/-1,-1/0,3/-3,-3/0,2/-2,-2/

CwU-Adj: /-3,-3/0,1/0,-2/0,-4/-4,0/-4,0/-2,0/5,0/-3,-3/
CcwU-Adj: /3,3/-5,0/2,0/4,0/4,0/0,4/0,2/0,-1/3,3/
Adj-CcwU: /-3,-3/0,-1/0,-2/0,-4/0,-4/-4,0/-2,0/-5,0/-3,-3/
Adj-CwU: /3,3/5,0/2,0/4,0/0,4/0,4/0,2/0,1/3,3/
```

[How to Solve the Square-1 | Tutorial](https://www.youtube.com/watch?v=5b291Cbvbl0) by DGCubes - Jun 25, 2016

```
Cubeshape: / -2, -4 / -1, -2 / -3, -3 /
Edge orientation: (1, 0 / 0, -3 / 0, -3 / -1, -1 / 1, 4 / 0, 3 /
Corner permutation: / 3, -3 / -3, 0 / 0, 3 / 0, -3 / 0, 3 /
Edge permutation: (-2, 0 / 3, 0 / -1, -1 / -2, 1 /
Parity: / -3, 0 / 0, 3 / 0, -3 / 0, 3 / 2, 0 / 0, 2 / -2, 0 / 4, 0 / 0, -2 / 0, 2 / -1, 4 / 0, -3 / 0, 3)
Swap layers: / 6, 6 /
Equator flip: / 6, 0 / 6, 0 / 6, 0) 
```

### Guides

- [How to Solve a Square-1](http://brandonlin.com/cubing/sq1tutorial.html) by Brandon Lin

- [Square-1 Tutorial](http://andrewknelson.com/square-1-tutorial/) by Andrew K. Nelson

- [(Back to) Square One / Cube 21](https://www.jaapsch.net/puzzles/square1.htm#s2m1) on Jaap's Puzzle Page

- [Square-1 Solution](http://www.cubezone.be/square1.html) on Lars Vandenbergh's CubeZone


### Algorithms

- [EO and CP Algorithms](http://brandonlin.com/cubing/eocp.html) by Brandon Lin

- [EP List](https://docs.google.com/spreadsheets/d/16lJ3YvrVJOi6AxkrM2W4MfRVQCbJWiKd_yjCTaMs8QA/edit#gid=0) by Charlie Stark

- [Square-1](http://algdb.net/puzzle/sq1) on AlgDB.net


### Forums

- [The "Square-1 Help / Alg Sharing" thread](https://www.speedsolving.com/forum/threads/the-square-1-help-alg-sharing-thread.37858/) on Speedsolving.com


