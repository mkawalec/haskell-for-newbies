##  let's create some types

    data Maybe a = Nothing | Just a

    data RecordContainer = RecordContainer {
        name :: Text,
        rank :: Int,
        isActive :: Bool
    }

    > let wrappedVal = Just "hello"
    > :t wrappedVal
    wrappedVal :: Maybe Text

    > let container = RecordContainer "Michał" 0 True
    > let modifiedContainer = container { rank = 5 }
