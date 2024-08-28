## introduction + example
first step is to put 8 dashes of course
`____ ____`
1 byte is 8 bits is why
MSB is the sign recall that
If +, the rest of the bits is the magnitude
If -, the rest of the bits are ***NOT*** the magnitude

so how do we convert +27 to 1s complement?
well it was `0001 1011`!
and in b16 it was `1B`

and when it was -27
we find the magnitude first we magnitude 7 leftover bits
`001 1011`
which is 27
and the NOT(Magnitude) of it is `110 0100`
and then inserting the MSB in the front it turns into
`1110 0100`
since the MSB is negative and the rest is the NOT magnitude
then we convert `1110` to `E` and `0100` to `4`
so the answer is `E4`
But if we check our work E4 in decimal is = to
$$ 14 \cdot 16 = 224 $$
$$ 4 \cdot 1 = 4 $$
$$ 224 + 4 = 228 $$
228 isn't our answer...
well actually remember it is out of range of our `sbyte` type so we need to bring it back into the `sbyte` range of `-128 to 127` by **subtracting 255** from 228 which gives us -27 again.
basically subtracting here un-nots `or unknots?` our value.

## pros n cons
### disadvantages
- it sucks to calculate remember 2 zeros
- bin arith doesn't work
- bin comp doesn't work
## advantages
- i guess there are none?