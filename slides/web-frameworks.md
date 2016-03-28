##  web frameworks

- `yesod` is a 'complete', big, RoR-like web framework for people who
    need their batteries
- `scotty` is a simple, Flask-like library that effectively binds
    functions to endpoints


    main = scotty 3000 $ do
        get "/:word" $ do
            beam <- param "word"
            html $ mconcat ["<h1>Scotty, ", beam, " me up!</h1>"]

