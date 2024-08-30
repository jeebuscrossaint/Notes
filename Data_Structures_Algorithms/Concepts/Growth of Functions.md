## introduction
- big O notation
- big O estimates for important functions
- big omega
- big theta notation

we want to make sure functions can handle larger and larger inputs

## big-O notation
`Definition: let f and g be functions from the set of integers or the set of real numbers to the set of real numbers. We say that f(x) is O(g(x)) if there are constants C and k such that:`
$$ |f(x)| \leq C|g(x) | $$
`whenever x > k`

- this is read as "f(x) is big O of g(x)" or "g asymptotically dominates f"
- the constants **C** and **k** are called witnesses