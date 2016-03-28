##  Strong static typing

- removes failures occuring from wrong data flow
- a type checker that works for you, not against you


    data AContainer = AContainer Integer
    data BiggerContainer = BiggerContainer Text Bool
    data Maybe a = Nothing | Just a

    data RecordContainer = RecordContainer {
        name :: Text,
        rank :: Int,
        isActive :: Bool
    }

