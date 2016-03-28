##  lists

Lists are not any special data type, we can define our own lists like:

    data List a = Nil | Cons a (List a)
    > :t Cons 1 (Cons 4 Nil)
    Cons 1 (Cons 4 Nil) :: Num a => List a

In real programs `Nil` is defined with a `[]` operator and `Cons` is `:`

    > :t 1 : 2 : 3 : []
    1 : 2 : 3 : [] :: Num a => [a]

