##  typeclasses

    addOne :: Num a => a -> a
    addOne x = x + 1

    class  Num a  where
        (+), (-), (*)       :: a -> a -> a
        negate              :: a -> a
        abs                 :: a -> a
        signum              :: a -> a
        fromInteger         :: Integer -> a

        x - y               = x + negate y
        negate x            = 0 - x
