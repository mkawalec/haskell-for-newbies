##  purity

- all of what we seen adds up to make most of our programs pure
- that means side effects can only exist in functions marked as impure


    impure :: IO ()
    impure = print "hey user"

what if we tried to make a pure version?

    <interactive>:25:12:
        Couldn't match expected type ‘()’ with actual type ‘IO ()’
        In the expression: print "a" :: ()
        In an equation for ‘pure’: pure = print "a" :: ()


