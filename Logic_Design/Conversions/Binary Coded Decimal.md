BCD expresses each decimal digit independently in hex or binary.
- BCD handles 1 digit decimal digit at a time to display to humans
- 1 decimal digit = 4 bits = 1 hex digit
- A B C D E F are not used in BCD only 0 - 9
- $$ 15_{BCD 16} = 0001 0101_{BCD 2} = 15_{10} $$
- $$ 15_{10} = 0001 0101_{BCD 2} = 15_{BCD 16} $$

![[Pasted image 20240825120132.png]]

## Binary Addition
0+0=0 sum=0 carry=0
0+1=1 sum=1 carry=0
1+0=1 sum=1 carry=0
1+1=10 sum=0 carry =1
when an input carry = 1 due to a previous result, the rules are
1 + 0 + 0 = 01 sum=1 carry =0
1 + 0 + 1 = 10 sum=0 carry =1
1 + 1 + 0 = 10 sum=0 carry = 1
1 + 1 + 1 = 11 sum=1 carry = 1

--- example: 
add the binary numbers 00111 and 10101 and show the decimal addition
00111 -> 7
10101 -> 21
______ 
11100 -> 28

