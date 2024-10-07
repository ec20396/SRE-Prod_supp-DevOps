# Activity: File Permissions in Linux

## Part A: Managing Users and Permissions

1. **Create a new user:**
    ```bash
    sudo adduser orderbook
    ```
    _Output:_
    No output

2. **Set the user's password:**
    ```bash
    echo 'orderbook:Hayri1' | sudo chpasswd
    ```
    _Output:_
    No output

3. **Expire the password:**
    ```bash
    sudo passwd --expire orderbook
    ```
    _Output:_
    ```
    passwd: password changed.
    ```

4. **Edit the sudoers file:**
    ```bash
    sudo visudo
    sudo EDITOR=vim visudo
    ```
    _Output:_
    No output

5. **Switch to the new user and change the password:**
    ```bash
    su orderbook
    ```
    _Output:_
    ```
    You are required to change your password immediately (administrator enforced).
    Changing password for orderbook.
    Current password:
    New password:
    Retype new password:
    ```

6. **Create a directory as the new user:**
    ```bash
    mkdir /home/test
    ```
    _Output:_
    ```
    mkdir: cannot create directory ‘/home/test’: Permission denied
    ```

7. **Create the directory with elevated permissions:**
    ```bash
    sudo mkdir /home/test
    ```
    _Output:_
    No output

8. **List directory contents:**
    ```bash
    ls -l /home
    ```
    _Output:_
    ```
    total 12
    drwxr-x--- 18 Hayri-Olcay Hayri-Olcay 4096 Aug  9 09:30 Hayri-Olcay
    drwxr-x---  2 orderbook            orderbook            4096 Aug  8 15:09 orderbook
    drwxr-xr-x  2 root                 root                 4096 Aug  9 09:30 test
    ```

9. **Add the `orderbook` user to the `admins` group:**
    ```bash
    sudo groupadd admins
    sudo usermod -a -G admins orderbook
    groups orderbook
    ```
    _Output:_
    ```
    orderbook : orderbook users admins
    ```

10. **Switch to the new user and attempt to create a file:**
    ```bash
    su orderbook
    touch /home/test/test.txt
    ```
    _Output:_
    ```
    touch: cannot touch '/home/test/test.txt': Permission denied
    ```

11. **Change group ownership and permissions of the directory:**
    ```bash
    sudo chgrp -R admins /home/test
    sudo chmod 771 /home/test
    sudo chmod g+w /home/test
    ```
    _Output:_
    No output

12. **Create the file again:**
    ```bash
    touch /home/test/test.txt
    ```
    _Output:_
    No output

13. **List contents of the `/home/test` directory:**
    ```bash
    ls -l /home/test
    ```
    _Output:_
    ```
    total 0
    -rw-rw-r-- 1 orderbook orderbook 0 Aug  9 09:34 test.txt
    ```

14. **Change ownership of the directory:**
    ```bash
    sudo chown -R orderbook /home/test
    ls -l /home/test
    ```
    _Output:_
    ```
    total 0
    -rw-rw-r-- 1 orderbook orderbook 0 Aug  9 09:34 test.txt
    ```

15. **Create a script in the directory:**
    ```bash
    cat << EOF > /home/test/orderbook.sh
    echo "welcome to orderbook"
    echo "Anyone can execute this script!!!"
    echo "But not everyone can edit it"
    EOF
    ```
    _Output:_
    No output

16. **Change script permissions:**
    ```bash
    chmod a+x+r /home/test/orderbook.sh
    chmod o+x+r /home/test/orderbook.sh
    chmod 755 /home/test/orderbook.sh
    ```
    _Output:_
    No output

17. **Edit and execute the script:**
    ```bash
    vi /home/test/orderbook.sh
    bash /home/test/orderbook.sh
    ```
    _Output:_
    ```
    welcome to orderbook
    Anyone can execute this script!!!
    But not everyone can edit it
    ```

---

This summarizes the commands used during the activity and their corresponding outputs.
