Convert 50.75 to binary:
The part in front of the decimal/radix point (50) in our case basically do repeated division upon it by 2. i.e. 
$$ 50/2 = 25r0 \rightarrow 25/2 = 12r1 \rightarrow 12/2 = 6r0 \rightarrow 6/2 = 3r0 \rightarrow 3/2 = 1r1 \rightarrow 2/1 = 0r1 $$
Then you take the remainders in reverse order so you get
**110010** as the part in front of decimal.

Now to do the .75 you do repeated multiplication:
$$ .75 \cdot 2 = 1.50 \rightarrow .50 \cdot 2 = 1.00 $$
And in the same reverse order the numbers behind the radix point are:
**.11**.
Giving us a final answer of:
$$ \large{110010.11} $$
You could also just do this:
![[Pasted image 20240825102359.png]]

![[Pasted image 20240825102527.png]]

## Reverse Engineering method
Another way of converting from decimal to binary is the reverse engineering method:
![[Pasted image 20240825103726.png]]
