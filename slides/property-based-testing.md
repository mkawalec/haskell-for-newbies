##  property based testing


- the boring tests are written for us, so what do we test?
- we can test logic
- or we can have the computer find a minimal failing case for us!


    propIdempotent xs = sort (sort xs) == sort xs
    > quickCheck propIdempotent
    +++ OK, passed 100 tests.

    [1,5,-1,3,6]
