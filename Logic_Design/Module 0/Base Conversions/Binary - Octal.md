Convert 10101.01 (binary) to octal.
Notice that 8 is a power of 2. Specifically 2^3.
Therefore:
Every 3 binary digits(bits) converts to 1 octal digit.
Therefore 7 is the largest octal digit.
(0 1 2 3 4 5 6 7)

Start at the radix point, group in groups of 3
Zero fill if needed
Basically so the radix point behind is only .01 but we need to add a third zero to make it work so it becomes .010
Therefore now our binary number is 010 | 101 | . | 010
Each number in each grouping has one could say a header of 4 2 1
So in the first portion 010 it could be 0 -> 4 1 -> 2 1 -> 0 therefore the value of it is 2
The second group could be 1 -> 4 0 -> 0 1 -> 1 to a value of 5 and the last group is the same numeration of the first one so its value is 2.
Therefore the answer is going to be **25.8**
