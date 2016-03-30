##  STM

We can implement way more complex effects simply with the type system.
Consider that:

    data Env = Env {
        counter :: TVar Int,
        chan :: TChan Text
    }

    modify :: Env -> STM ()
    modify env = do
        modifyTVar (counter env) (\x -> x + 1)
        writeTChan (chan env) "I've added one"

    > ourChan <- newTChanIO
    > let ourEnv = Env 0 ourChan
    > atomically (modify ourEnv)
    > readTVar (counter ourEnv)
    1
