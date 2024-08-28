## introduction

different notations are used in computers to rep signed numbers
### whole numbers (on quiz 0b)
signed magnitude
1's complement
2's complement

### floating points
exponential notation
excess N notation

## sign magnitude notation
1 byte is 8 bits and half a byte ( 4 bits ) is a nybble!
most significant bit (msb) is the first bit 
so the first underscore below
the rest of the number tells you what magnitude it is
``` 
(MSB) -> [_]___ ____
		  ^ - sign
```

all the other bits are given in base 2 and declare the magnitude of the number or the `| absolute value |` of the number.
### positive number
- mark number of bit places
- sign (msb) is 0
>rest of the number is the magnitude in binary
  using place value or repeated division

### negative number
- mark number of bit places
- sign (msb) is 1
>rest is the number is magnitude in binary
>using place value or repeated division

### example (positive)
- 1 byte is 8 bits
- lets represent the number +27 in hexadecimal so we can put it in memory
1. mark the number of bit places
- you know the first is sign rest is bits in binary
2. sign (msb)
- you know the msb is 0 since it is positive
3. rest of the number you convert the magnitude to binary using the methods

+27_10 = __ 2 = __  16
so using place values:
27 - 16 = 11
`0001 ____`
(first is 0 bcuz sign, then last one here represents 2^4 or 16)
11 - 8 = 3
`0001 1___`
cant take 4 from 3
`0001 10__`
3 - 2 = 1
`0001 101_`
1 - 1 = 0
`0001 1011`
represents +27 in binary
now the quick bin - hex conversion
0001 = 1
1011 = B
`+27 in binary is equal to 1B in hexadecimal, which is our answer.`

### example (negative)
lets do the same thing but with `-27`
so the first digit is 1 since it is negative
`1___ ____`
we already calculated the rest of the number so
`1001 1011` is our answer in binary
now the hexadecimal conversion is a little *finnicky*
so the first portion is now equal to 9 and the last part is 11 so B
so now the answer is `9B`
even though it is the SAME absolute value, `|27|`
but if we checked it we would find 
$$ 9 \cdot 16 = 144 $$
$$ 11 \cdot 1 = 11 $$
$$ 144 + 11 = 155 $$
`155` is NOT our answer, because it stack overflows the range of a `C lang` `sbyte` type which has range of `{ -128 to 127 }`. But it does not overflow the `byte` type which has range `{ 0 to 255 }` which means taking the difference between 255 and 127 means that if the number in hex is between `0 and 127` then the MSB is positive and if between `128 and 255` the MSB is negative

### pros n cons
#### advantage of sign magnitude notation:
- easy to convert
- thats about it

#### disadvantage of sign magnitude notation:
- two zeros `(+0 and -1)`
- `0000 0000 = +0 and 1000 0000 = -0`
- inefficient and confusing when doing arithmetic
- binary arithmetic ***DOES NOT WORK*** 
- binary comparison ***DOES NOT WORK***
#### why use this garbage then?
- for floats it is most common way to represent the `significand (also called the mantissa or coefficient)
- 

