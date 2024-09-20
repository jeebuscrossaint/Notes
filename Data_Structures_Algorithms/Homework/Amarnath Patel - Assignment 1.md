
**1a.**

```
procedure oddOrEvenCount(numbers)
    oddCount = 0
    evenCount = 0
    for each num in numbers
        if num % 2 == 0
            evenCount = evenCount + 1
        else
            oddCount = oddCount + 1
    if oddCount > evenCount
        return "odd"
    else if evenCount > oddCount
        return "even"
    else
        return "equal"

```

_____

**1b.**

```
procedure CosSim(A, B)
    dotProduct = 0
    normA = 0
    normB = 0

    n = length(A)

    for i from 1 to n
        dotProduct = dotProduct + A[i] * B[i]
        normA = normA + A[i] * A[i]
        normB = normB + B[i] * B[i]

    magnitudeA = sqrt(normA)
    magnitudeB = sqrt(normB)

    cosineSimilarity = dotProduct / (magnitudeA * magnitudeB)

    return cosineSimilarity

```

_____

**2a.**
$$ \text{The worst case runtime in Big-O notation is O} (\sqrt n) \space \text{because the most significant portion is the for loop that runs `sqrt n` times}$$

_____

**2b.**

$$ \text{The outer loop runs n - 1 times and the inner loop runs decreasingly for each iteration the outer loop takes, in this way: (n-1) + (n-2) + ... + 1 } \text{This is the sum of the first `n-1` integers, which follows: }  $$
$$ \frac{(n-1) \cdot n}{2} = O(n^2) $$
______

**2c.**
$$ \text{Each shuffle `shuffle()` and `isInOrder` operations take } O(n\cdot n!) \text{ or } O[(n+1)!] $$

_____

**3.**

$$ \text{In binary search the worst-case and average-case runtime complexity is the same, and the worst case in binary search is } O(log(n)) \text{ therefore the average-case runtime complexity is also } O(log(n)). $$
_____

**4a.**

$$ \text{No it does not give a correct solution for making change of n cents if a nickel was worth 6} \textcent  \text{ because the greedy algorithm in an example of using 12 cents it would use 10 cents (dime) 1 cent (2 pennies) totaling to 3 coins whereas the correct solution/optimal solution would be 6 cents (2 nickels) totaling to 2 coins.}$$

_____

**4b.**

```
procedure FractionalKnapsack(weights array w, values array v, capacity W)
    n = length(w) 
    valuePerWeight = array of size n


    for i in 0 to n - 1
        valuePerWeight[i] = v[i] / w[i]


    sort(valuePerWeight, w, v)

    totalValue = 0
    for i in 0 to n - 1
        if W <= 0
            break
        

        if w[i] <= W
            W = W - w[i]
            totalValue = totalValue + v[i]
        else
            totalValue = totalValue + (v[i] / w[i]) * W
            W = 0 

    return totalValue
```

$$ \text{Alg takes 2 array weights and values and a weight limit capacity. The value per weight calc finds the value of the value-weight ratio for each item. They are sorted based on the ratio in descending order. The greedy selection iteravely gets items until the knapsack is full either taking the whole item or a fraction if it cant fit fully.} $$

_____

**5.**

```
procedure MaxIncreasingSum(arrays 2D array A, n, m)
    maxSum = 0
    previousSelected = infinity 

    
    for i in n - 1 down to 0
        currentMax = -1 
        selectedValue = -1 

        for j in 0 to m - 1
            if A[i][j] < previousSelected and A[i][j] > currentMax
                currentMax = A[i][j]
        
        if currentMax == -1
            return 0
        
        selectedValue = currentMax
        maxSum = maxSum + selectedValue
        previousSelected = selectedValue

    return maxSum
```

$$ \text{Algorithm takes a 2d array A with dimensions n x m where n is arrays and m is their size. It moves backwards to ensure it is strictly increasing. In each array it finds the max value that is less than the prev value. It gathers  the max values to get the total sum. If a good selection is not made at any time the func returns 0.} $$
