##  threading model

- very lightweight threads using only the CPUNUM system threads
- it's actually cheaper to spawn a thread than play with an event loop
    (and threads are isolated!)

<img src='resources/threads.png'/>
