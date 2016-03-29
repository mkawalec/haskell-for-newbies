##  Parser combinators

- Build parsers from small parts. `attoparsec` & `parsec`


    emailAddressParser :: Parser EmailAddress
    emailAddressParser = nameAddrParser <|> addrSpecParser

    nameAddrParser :: Parser EmailAddress
    nameAddrParser = do
      label <- takeWhile (/= '<')
      _ <- char '<'
      address <- takeWhile (/= '>')
      _ <- char '>'
      return $ EmailAddress address (Just $ strip label)

    addrSpecParser :: Parser EmailAddress
    addrSpecParser = do
      address <- takeWhile (\c -> c /= '\r' && c /= ',')
      return $ EmailAddress address Nothing
