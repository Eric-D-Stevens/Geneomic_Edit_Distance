# Gene Sequence Edit Distance Using Dynamic Programming 

This set of scripts takes a file of formatted gene sequences and outputs the minimum
'edit distance' based on a cost matrix that is included in this repository. Usage of 
dynamic programming techniques allows for the implementation of an algorithm with a 
time complexety of O(mxn) where m and n are the lengths of the input sequences.

## Usage

To run the script, simply enter `Python2.7 EditDistance.py`

### Prerequisites

This script was written for Python 2.7.14 and requires no libraries.

##Input and Output 

### Input

#### Gene Sequences

While there are no command line inputs to run this script, the program does rely on two
file inputs for its operation. The first file is named `imp2input.txt`. This file contains 
the input gene sequences for which the edit distances will be calculated. The format for 
this file is as follows:

```
CGCAATTCTGAAGCGCTGGGGAAGACGGGT,TATCCCATCGAACGCCTATTCTAGGAT
AGTTGTGAAAGAACAAGCGCACAATATTGCCGCGCCGAAAGCT,TTCTTTCATTATTCAAATGTATAGTTTAGAGCGTTAA
...
...
TAAACCTAGGCATGTCTGTTTCG,TATAGAGCAGGTTCAAAACCAATGCGCTTCAATA
```

The two comma seperated strings are the two gene sequences that will be compared to one
and other to calculate the edit distance.

#### Cost Table

The next input is the 'cost table'. The cost table is a text file that represents a matrix 
is used to value the cost of taking individual edit actions. An example of the format of 
this table is as follows:

```
*,-,A,T,G,C
-,0,1,2,1,3
A,1,0,1,5,1
T,2,1,0,9,1
G,1,5,9,0,1
C,3,1,1,1,0
```

As we can see, the cost table consists of '-' character followed by the four letters that 
that are used to represent the chemical makeup of a gene sequence. These values are laid end 
to end to create a symmetric matrix that will serve as a look up table when performing edit 
operations. The '-' symbol in table is a lookup for doing an insert operation.

### Output

xxx
