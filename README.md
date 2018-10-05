# truth-table-silliness

possible inputs:
a	b
1	1
1	0
0	1
0	0
outputs from upto 5 Nand gates/chips:
(F is false, T is true, N is for Nand, a & b are as above, 
and NP is for Not(previous column),
which means hooking up the previous output to both inputs of a single Nand gate)

(number of Nands)
0|0|0|0| 1 | 2 | 1 | 1 |   3   |4 | 2  |3 | 2  | 3|  4  |5
===========================================================
 | | | |   |   |   |   |       |  |    |  |    |  | a b |
 | | | |   |   |   |   |a a b b|  | a b|  |a b |  |a N b|
 | | | |a b|   |a a|b b| N_ _N |  |a N |  | N b|  | N N |
T|F|a|b| N | NP| N | N |   N   |NP| N  |NP|  N |NP|  N  |NP
1|0|1|1| 0 | 1 | 0 | 0 |   1   |0 | 1  |0 |  1 |0 |  0  |1
1|0|1|0| 1 | 0 | 0 | 1 |   1   |0 | 0  |1 |  1 |0 |  1  |0
1|0|0|1| 1 | 0 | 1 | 0 |   1   |0 | 1  |0 |  0 |1 |  1  |0
1|0|0|0| 1 | 0 | 1 | 1 |   0   |1 | 1  |0 |  1 |0 |  0  |1
