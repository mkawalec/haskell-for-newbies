##  higher order functions

We can have functions accept other functions

    > :t map
    map :: (a -> b) -> [a] -> [b]

Multiple ways of using this pattern:

    > let awesomeList = [1,2,3,0,5]

    > let mult x = x * 2
    > map mult awesomeList
    [2, 4, 6, 0, 10]

    > map (\x -> x * 2) awesomeList

    > map (\_ -> "foo") awesomeList
    ["foo","foo","foo","foo","foo"]
