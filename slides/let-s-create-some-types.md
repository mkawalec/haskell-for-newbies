##  let's create some types

    data Maybe a = Nothing | Just a

    data RecordContainer = RecordContainer {
        name :: Text,
        rank :: Int,
        isActive :: Bool
    }

    > let wrappedVal = Just "hello"
    > :t wrappedVal
    wrappedVal :: Maybe [Char]

    > let container = RecordContainer "Michal" 0 True
    > let modifiedContainer = container { rank = 5 }
