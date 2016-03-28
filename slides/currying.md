##  currying

Let's take a look on the type of map

    > :t map
    map :: (a -> b) -> [a] -> [b]

We can partially apply it and get a function that accepts a list

    > :t map (*2)
    map (*2) :: Num b => [b] -> [b]

And apply it completely to get a result

    > :t map (*2) [1,2]
    map (*2) [1,2] :: Num b => [b]
