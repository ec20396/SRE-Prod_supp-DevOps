# Activity: Advanced Commands

## Part A: File and Directory Management

1. **Clean up your home directory:**
    If you have not been doing this all along, clean up your home directory removing any files you no longer need.

2. **Run the fixGenerator.sh script in your home directory:**
    ```bash
    ./fixGenerator.sh &
    ```
    _Output:_
    No output

## Part B: Log File Manipulation

1. **Create a directory named logs:**
    ```bash
    mkdir ~/logs 
    ```
    _Output:_
    No output

2. **Move the log output from the fixGenerator script into the logs directory:**
    Be sure the script has finished before doing this.
    ```bash
    mv fixlog2024039823001.log logs/.
    ```
    _Output:_
    No output

3. **Replace all instances of MTHREE in the file with M3 and put the output into a new file named fixlog2.log in the logs directory:**
    ```bash
    cat fixlog2024039823001.log | sed 's/MTHREE/M3/g' > logs/fixlog2.log
    ```
    _Output:_
    No output

4. **Pull all fill messages from fixlog2.log and put the output into a new logfile named fills.log:**
    (You may need to look up how to tell if a message is a fill.)
    ```bash
    grep 35=8 logs/fixlog2.log | grep -v 32=0 > logs/fills.log
    ```
    _Output:_
    No output

5. **Pull all cancel acknowledgment messages (39=4) from fixlog2.log into a new log named cancels.log:**
    ```bash
    grep 39=4 logs/fixlog2.log > logs/cancels.log
    ```
    _Output:_
    No output

6. **Create a new log file named partialFills.log and add the partial fills from fills.log to the new file:**
    ```bash
    grep 39=1 logs/fills.log > logs/partialFills.log
    ```
    _Output:_
    No output

7. **Create a new file from the partial fill log with specific tags using awk:**
    The tags should be: Symbol (55); orderID (11); side (54); fill price (31); fill quantity (32); execution id (17).
    ```bash
    awk '{print $7, $9, $13, $10, $15, $16}' logs/partialFills.log > logs/parsedPartialFills.log
    ```
    _Output:_
    No output

8. **Edit the file to remove the first part of every fix tag and convert to a comma-separated list:**
    Use an editor to make these changes.

9. **Add a row of column headers to the file:**
    The headers should be Symbol, OrderID, Side, Price, Qty, and ExecID.
    Save the file as `Hayri.module10.csv` in the location specified by your instructor.

10. **Make a copy of the cancels file and name it cancels2.log:**
    ```bash
    cp logs/cancels.log logs/cancels2.log 
    ```
    _Output:_
    No output

11. **Edit the cancels2.log file to modify the first symbol value:**
    Find the first symbol (tag 55) in the first line and add the letter A to the beginning of the value.
    (If it was 55=GOOG, it will become 55=AGOOG.)

12. **Run a difference between the original cancels file and the new file:**
    ```bash
    diff logs/cancels.log logs/cancels2.log 
    ```
    _Output:_
    Displays the differences between the two files.

13. **Run the history command and save it to an output file:**
    Save the output as `YYMMDD.module10` in the directory specified by your instructor.
    ```bash
    history > YYMMDD.module10
    ```
    _Output:_
    No output

