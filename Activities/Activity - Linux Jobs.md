# Activity: Linux Jobs

## Part A: Managing Jobs

1. Run a job in the foreground:
    ```bash
    sleep 60
    ```
    _Output:_
    No output

2. Run a job in the background:
    ```bash
    sleep 200 &
    ```
    _Output:_
    No output

3. View all jobs running in the background:
    ```bash
    jobs
    ```
    _Output:_
    ```
    [1]+  Running                 sleep 200 &
    ```

4. Send a running job from the foreground to the background:
    ```bash
    sleep 50
    # now enter Ctrl+z
    ```
    _Output:_
    ```
    [2]+  Stopped                 sleep 50
    ```

5. View the jobs again:
    ```bash
    jobs
    ```
    _Output:_
    ```
    [1]+  Running                 sleep 200 &
    [2]+  Stopped                 sleep 50
    ```

6. Start the last job in the background:
    ```bash
    bg
    ```
    _Output:_
    ```
    [2]+ sleep 50 &
    ```

7. Use the job number to start a job:
    ```bash
    sleep 100
    # now enter Ctrl+z
    sleep 200
    # now enter Ctrl+z
    sleep 300
    # now enter Ctrl+z
    jobs
    # prints something similar to
    #[1]-  Stopped                 sleep 100
    #[2]-  Stopped                 sleep 200
    #[3]+  Stopped                 sleep 300
    bg 2
    ```
    _Output:_
    ```
    [2]+ sleep 200 &
    ```

8. Start multiple jobs by their numbers:
    ```bash
    bg 1 3
    ```
    _Output:_
    ```
    [1]- sleep 100 &
    [3]+ sleep 300 &
    ```

9. Terminate a job:
    ```bash
    # kill job number 1
    kill %1
    # kill job number 2 and 3.
    kill %2 %3
    ```
    _Output:_
    No output

10. Bring a job back to the foreground:
    ```bash
    sleep 200 &
    # [1] 19085 # This is job number 1
    fg 1
    ```
    _Output:_
    ```
    sleep 200
    ```

## Part B: Using Screen

1. Start a screen session:
    ```bash
    screen
    ```
    _Output:_
    No output

2. Run the command below, then press `Ctrl+a` and `d` to exit the screen:
    ```bash
    while true; do echo "screen 1..."; sleep 5; done
    # To exit this screen press Ctrl+a, then d
    ```
    _Output:_
    ```
    screen 1...
    ```

3. Start another screen session and exit:
    ```bash
    screen
    while true; do echo "screen 2..."; sleep 5; done
    # To exit this screen press Ctrl+a, then d
    ```
    _Output:_
    ```
    screen 2...
    ```

4. List your screen sessions:
    ```bash
    screen -list
    ```
    _Output:_
    ```
    There are screens on:
        221271.pts-0.ip-172-31-24-77 (Detached)
        193073.pts-1.ip-172-31-24-77 (Detached)
    ```

5. Re-enter a screen session:
    ```bash
    exit
    # log back, make sure the numbers match the results of screen -list
    screen -r 193073
    # Ctrl+a, d
    screen -r 221271
    # Ctrl+a, d
    ```
    _Output:_
    No output

6. Close out a screen session:
    ```bash
    # do this for your screen sessions.
    screen -X -S 193073 quit
    ```
    _Output:_
    No output
