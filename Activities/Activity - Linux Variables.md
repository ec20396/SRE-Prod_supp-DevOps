# Activity: Linux Variables

## Part A: Environment Variables

1. Print all of the environment variables in your system:
    ```bash
    printenv
    ```
    _Output:_
    A list of all the environment variables currently set in your system.

2. Add an environment variable to your system and then echo the variable to confirm it is set:
    ```bash
    export name=Hayri
    echo "My name is $name"
    ```
    _Output:_
    ```
    My name is Hayri
    ```

3. Test what happens when single quotes are used:
    ```bash
    echo 'My name is $name'
    ```
    _Output:_
    ```
    My name is $name
    ```
    _Note:_ The `$name` variable is not expanded because single quotes prevent variable expansion in the shell.

4. Create a variable without the `export` command and display its value:
    ```bash
    name=Varelis
    echo $name
    ```
    _Output:_
    ```
    Varelis
    ```

5. Write the following script and observe the output:
    ```bash
    export name=Hayri
    lname=Varelis
    echo 'echo $name' > test.sh # prints Hayri when executed
    echo 'echo $lname' >> test.sh # does not print anything
    chmod +x test.sh
    ```
    _Output:_
    No output after creating the script. The next step will show the output when executing it.

6. Execute the script:
    ```bash
    ./test.sh
    ```
    _Output:_
    ```
    Hayri
    ```
    _Note:_ Only variables created with `export` are available in subprocesses, hence `lname` is not displayed.

7. Log out and log back in, then check the variables `name` and `lname`:
    ```bash
    echo $name
    echo $lname
    ```
    _Output:_
    No output because variables are cleared after logging out.

## Part B: Persisting Environment Variables

1. Add the `name` variable to your `~/.bash_profile` so it persists across sessions:
    ```bash
    echo 'export name=Hayri' >> ~/.bash_profile
    exit
    # Log in again
    # or use the source command instead of logging out and back in:
    source ~/.bash_profile
    ```
    _Output:_
    No output.

2. Confirm that the `name` variable is set after logging in again:
    ```bash
    echo $name
    ```
    _Output:_
    ```
    Hayri
    ```

3. Add a custom directory to your `PATH` and verify:
    ```bash
    mkdir -p $HOME/.local/bin
    echo 'export PATH="$PATH:$HOME/.local/bin"' >> ~/.bash_profile
    source ~/.bash_profile
    echo $PATH
    ```
    _Output:_
    The updated `PATH` variable, which now includes `$HOME/.local/bin`.

## Part C: Working with Scripts

1. Create a script in `.local/bin` and make it executable:
    ```bash
    cat << EOF > $HOME/.local/bin/welcome
    echo "Welcome \$USER"
    [[ \$1 == "date" ]] && echo "Today is \$(date)"
    EOF
    chmod +x $HOME/.local/bin/welcome
    ```
    _Output:_
    No output.

2. Run the script:
    ```bash
    welcome
    welcome date
    ```
    _Output:_
    ```
    Welcome <your-username>
    Today is <current-date>
    ```

3. Create an alias for the script and make it persistent:
    ```bash
    echo 'alias wd="welcome date"' >> ~/.bash_profile
    source ~/.bash_profile
    wd
    ```
    _Output:_
    ```
    Welcome <your-username>
    Today is <current-date>
    ```

## Part D: Additional Exercises

1. Create a new directory for your scripts:
    ```bash
    mkdir ~/scripts
    cd ~/scripts
    ```
    _Output:_
    No output.

2. Write a "Hello World" Python script and execute it:
    ```bash
    cat << EOF > hello.py
    #!/usr/bin/env python3
    print("Hello World of Python")
    EOF
    chmod +x hello.py
    ./hello.py
    ```
    _Output:_
    ```
    Hello World of Python
    ```

3. Add the `scripts` directory to your `PATH`:
    ```bash
    echo 'PATH="$PATH:$HOME/scripts"' >> ~/.bash_profile
    source ~/.bash_profile
    echo $PATH
    ```
    _Output:_
    The updated `PATH` variable, which now includes `$HOME/scripts`.

4. Execute the Python script from any directory:
    ```bash
    hello.py
    ```
    _Output:_
    ```
    Hello World of Python
    ```

5. Create a symbolic link to the `python3` binary named `py`:
    ```bash
    sudo ln -s /usr/bin/python3 /usr/bin/py
    ```
    _Output:_
    No output.

