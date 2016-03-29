##  Signalling adversity

How do we signal that a value may be missing? Use `Maybe`

    data Maybe a = Nothing | Just a

or better `Either` for an error message

    data Either a b = Left a | Right b

    multIfLucky :: Int -> Either Text Int
    multIfLucky 42 = Right (42 * 2)
    multIfLucky _  = Left "you're unlucky"
