##  recursion

Factorial is a nice example

	factorial :: Integer -> Integer
	factorial 0 = 1
	factorial n = n * factorial (n - 1)

    > factorial 2
    2
    > factorial 4
    24

	> map factorial [1..10]
    [1,2,6,24,120,720,5040,40320,362880,3628800]
