##  low on boilerplate

Lambdas without the cruft

    > map (\x -> "Hello " ++ x) ["Batman", "Watman"]
    ["Hello Batman","Hello Watman"]

Types are separate from function definitions

    greet :: Text -> Text
    greet name = append "Hello " name
