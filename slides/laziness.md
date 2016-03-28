##  laziness

- harder to digest at first, but very useful in real-life programs
- `[1..]` is actually an infinite sequence
- but we have finite time and memory. So we can work with infinite data
    as long as we don't evaluate it

let's write a fibbonacci

    > :t scanl
    scanl :: (b -> a -> b) -> b -> [a] -> [b]

    > let fib = 1 : (scanl (+) 1 fib)
    > take 10 fib
    [1,1,2,3,5,8,13,21,34,55]

