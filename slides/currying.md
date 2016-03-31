##  currying

Let's take a look on the type of map

    > :t map
    map :: (a -> b) -> [a] -> [b]

We can partially apply it and get a function that accepts a list

    > let parap = map (\x -> x * 2)
    > :t parap
    parap :: Num b => [b] -> [b]

And apply it completely to get a result

    > parap [1,2]
    [2,4]

Add a javascript example
