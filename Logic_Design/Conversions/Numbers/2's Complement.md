## introduction
if +, the rest is magnitude
if -, NOT(Magnitude) + 1
`____ ____`

so for +27
it is `0001 1011`
which is the same how it was in the original sign magnitude notation 
and in hex is of course `1B`

now for -27
so we take the magnitude
`001 1011`
and then NOT it (1s to 0 and 0s to 1s)
`110 0100`
and then add a 1 to the ***end*** of the magnitude
`1100101`
and then throw in the front the sign of course since negative
`1110 0101`
which ends up being `E5`
but if we check again
$$ 14 \cdot 16 = 224 $$
$$ 5 \cdot 1 = 5 $$
$$ 224 + 5 = 229 $$
and in 2s complement we **subtract by 256** (in 1s we subtracted by 255) and this will unNOT all the bits back
$$ 229 - 256 = -27 $$

## pros n cons
### advantages
- only one zero `0000 0000`
- has largest range from -128 to 127
- bin arith works
![[Pasted image 20240827212120.png]]
### disadvantage
- more complex conversion
- bin comp does __not__ work all the time
- -128 `1000 0000` and +127 `0111 1111`
- only works comparing positive to positive and negative to negative
