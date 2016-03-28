##  Fibonacci

    > :t scanl
    scanl :: (b -> a -> b) -> b -> [a] -> [b]

    > let fib = 1 : (scanl (+) 1 fib)
    > take 10 fib
    [1,1,2,3,5,8,13,21,34,55]

Let's disect that per iteration:

    fib = 1 : 1
    fib = 1 : 1 : (1 + fib[0]) = 1 : 1 : 2
    fib = 1 : 1 : 2 : (2 + fib[1]) = 1 : 1 : 2 : 3
    fib = 1 : 1 : 2 : 3 : (3 + fib[2]) = 1 : 1 : 2 : 3 : 5

So we can work with bottoms as long as we only see their finite parts!
