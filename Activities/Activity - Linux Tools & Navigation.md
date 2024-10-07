1. Check the current version of Linux:
    ```bash
    uname -a
    ```
    _Output:_
    ```
    Linux Hayri-Olcay-VirtualBox 6.8.0-39-generic #39-Ubuntu SMP PREEMPT_DYNAMIC Fri Jul  5 21:49:14 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux
    ```

2. Check your current location in the file structure:
    ```bash
    pwd
    ```
    _Output:_
    ```
    /home/Hayri-Olcay/Desktop
    ```

3. Move up one folder:
    ```bash
    cd ..
    ```
    _Output:_
    No output (just moves up one directory level)

4. Check your location again:
    ```bash
    pwd
    ```
    _Output:_
    ```
    /home/Hayri-Olcay
    ```

5. List all the files with details. Try both of these commands to see how they are different:
    ```bash
    ls -l
    ```
    _Output:_
    ```
    total 1176
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   1056 Aug  6 11:44 avengers.Hayri.txt
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay     48 Aug  6 10:15 cron_test.log
    drwxr-xr-x 5 Hayri-Olcay Hayri-Olcay   4096 Aug  6 15:38 Desktop
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Documents
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Downloads
    -rwxr-xr-x 1 root                 root                   7350 Jul  1 23:57 fixGenerator.sh
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 102001 Aug  5 12:03 fixlog20240805120001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50349 Aug  5 12:33 fixlog20240805123001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51002 Aug  5 13:03 fixlog20240805130001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  54227 Aug  5 15:03 fixlog20240805150001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  48529 Aug  5 15:33 fixlog20240805153001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 101423 Aug  6 10:03 fixlog20240806100001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  52397 Aug  6 10:23 fixlog20240806102001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  52427 Aug  6 10:43 fixlog20240806104001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51222 Aug  6 11:03 fixlog20240806110001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50989 Aug  6 11:23 fixlog20240806112001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51304 Aug  6 11:43 fixlog20240806114001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay    324 Aug  6 11:45 fixlog20240806114555.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49851 Aug  6 11:49 fixlog20240806114601.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 104079 Aug  6 12:03 fixlog20240806120001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50911 Aug  6 12:23 fixlog20240806122001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50668 Aug  6 12:43 fixlog20240806124001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49468 Aug  6 14:23 fixlog20240806142001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49456 Aug  6 14:43 fixlog20240806144001.log
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Music
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.Hayri.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.log
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Pictures
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Public
    drwxrwxr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  5 11:56 scripts
    drwx------ 5 Hayri-Olcay Hayri-Olcay   4096 Aug  5 12:00 snap
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Templates
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Videos
    ```

    ```bash
    ls -ltr
    ```
    _Output:_
    ```
    total 1176
    -rwxr-xr-x 1 root                 root                   7350 Jul  1 23:57 fixGenerator.sh
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Videos
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Templates
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Public
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Pictures
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Music
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Downloads
    drwxr-xr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Documents
    drwxrwxr-x 2 Hayri-Olcay Hayri-Olcay   4096 Aug  5 11:56 scripts
    drwx------ 5 Hayri-Olcay Hayri-Olcay   4096 Aug  5 12:00 snap
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 102001 Aug  5 12:03 fixlog20240805120001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50349 Aug  5 12:33 fixlog20240805123001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51002 Aug  5 13:03 fixlog20240805130001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  54227 Aug  5 15:03 fixlog20240805150001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  48529 Aug  5 15:33 fixlog20240805153001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 101423 Aug  6 10:03 fixlog20240806100001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay     48 Aug  6 10:15 cron_test.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  52397 Aug  6 10:23 fixlog20240806102001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  52427 Aug  6 10:43 fixlog20240806104001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51222 Aug  6 11:03 fixlog20240806110001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50989 Aug  6 11:23 fixlog20240806112001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  51304 Aug  6 11:43 fixlog20240806114001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   1056 Aug  6 11:44 avengers.Hayri.txt
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay    324 Aug  6 11:45 fixlog20240806114555.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49851 Aug  6 11:49 fixlog20240806114601.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.Hayri.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay 104079 Aug  6 12:03 fixlog20240806120001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50911 Aug  6 12:23 fixlog20240806122001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  50668 Aug  6 12:43 fixlog20240806124001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49468 Aug  6 14:23 fixlog20240806142001.log
    -rw-rw-r-- 1 Hayri-Olcay Hayri-Olcay  49456 Aug  6 14:43 fixlog20240806144001.log
    drwxr-xr-x 5 Hayri-Olcay Hayri-Olcay   4096 Aug  6 15:38 Desktop
    ```

6. Change the directory to the root folder:
    ```bash
    cd /
    ```
    _Output:_
    No output (just changes directory to the root)

7. Check your location again:
    ```bash
    pwd
    ```
    _Output:_
    ```
    /
    ```

8. List all files in the current directory, sorted with the most recently-changed file at the bottom of the screen:
    ```bash
    ls -ltr
    ```
    _Output:_
    ```
    total 4009052
    drwxr-xr-x   2 root root       4096 Feb 26 12:58 bin.usr-is-merged
    drwxr-xr-x   2 root root       4096 Mar 31 10:00 sbin.usr-is-merged
    drwxr-xr-x   2 root root       4096 Apr  8 15:37 lib.usr-is-merged
    lrwxrwxrwx   1 root root          8 Apr 22 14:08 sbin -> usr/sbin
    lrwxrwxrwx   1 root root          9 Apr 22 14:08 lib64 -> usr/lib64
    lrwxrwxrwx   1 root root          7 Apr 22 14:08 lib -> usr/lib
    lrwxrwxrwx   1 root root          7 Apr 22 14:08 bin -> usr/bin
    drwxr-xr-x  12 root root       4096 Apr 24 11:47 usr
    drwxr-xr-x   2 root root       4096 Apr 24 11:47 srv
    drwxr-xr-x   2 root root       4096 Apr 24 11:47 mnt
    drwxr-xr-x  12 root root       4096 Apr 24 11:51 snap
    dr-xr-xr-x   2 root root       4096 Aug  4 01:32 cdrom
    drwx------   2 root root      16384 Aug  4 01:38 lost+found
    -rw-------   1 root root 4105175040 Aug  4 01:47 swap.img
    drwxr-xr-x   3 root root       4096 Aug  4 01:53 home
    drwxr-xr-x  15 root root       4096 Aug  5 09:43 var
    drwxr-xr-x   3 root root       4096 Aug  5 10:22 media
    drwxr-xr-x   3 root root       4096 Aug  5 10:23 opt
    drwxr-xr-x   3 root root       4096 Aug  5 10:24 boot
    drwxr-xr-x 144 root root      12288 Aug  5 11:45 etc
    drwx------   5 root root       4096 Aug  5 15:40 root
    dr-xr-xr-x  13 root root          0 Aug  6 22:09 sys
    dr-xr-xr-x 284 root root          0 Aug  6 22:09 proc
    drwxr-xr-x  20 root root       4240 Aug  6 22:10 dev
    drwxr-xr-x  36 root root        940 Aug  6 22:38 run
    drwxrwxrwt  19 root root       4096 Aug  6 22:46 tmp
    ```

9. Change back to your home directory:
    ```bash
    cd ~
    ```
    _Output:_
    No output (just changes directory to the home)

10. List all files, including the hidden files:
    ```bash
    ls -ltra
    ```
    _Output:_
    ```
    total 1288
    -rw-r--r--  1 Hayri-Olcay Hayri-Olcay    807 Mar 31 09:41 .profile
    -rw-r--r--  1 Hayri-Olcay Hayri-Olcay   3771 Mar 31 09:41 .bashrc
    -rw-r--r--  1 Hayri-Olcay Hayri-Olcay    220 Mar 31 09:41 .bash_logout
    -rwxr-xr-x  1 root                 root                   7350 Jul  1 23:57 fixGenerator.sh
    drwxr-xr-x  3 root                 root                   4096 Aug  4 01:53 ..
    drwx------  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:55 .ssh
    drwx------  4 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 .local
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Videos
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Templates
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Public
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Pictures
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Music
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Downloads
    drwxr-xr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  4 01:56 Documents
    -rw-r--r--  1 Hayri-Olcay Hayri-Olcay      0 Aug  4 02:12 .sudo_as_admin_successful
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay     66 Aug  5 11:52 .selected_editor
    drwxrwxr-x  2 Hayri-Olcay Hayri-Olcay   4096 Aug  5 11:56 scripts
    drwx------  5 Hayri-Olcay Hayri-Olcay   4096 Aug  5 12:00 snap
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay 102001 Aug  5 12:03 fixlog20240805120001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  50349 Aug  5 12:33 fixlog20240805123001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  51002 Aug  5 13:03 fixlog20240805130001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  54227 Aug  5 15:03 fixlog20240805150001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  48529 Aug  5 15:33 fixlog20240805153001.log
    -rw-------  1 Hayri-Olcay Hayri-Olcay     20 Aug  5 15:40 .lesshst
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay 101423 Aug  6 10:03 fixlog20240806100001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay     48 Aug  6 10:15 cron_test.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  52397 Aug  6 10:23 fixlog20240806102001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  52427 Aug  6 10:43 fixlog20240806104001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay    165 Aug  6 10:59 .wget-hsts
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  51222 Aug  6 11:03 fixlog20240806110001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  50989 Aug  6 11:23 fixlog20240806112001.log
    drwx------ 12 Hayri-Olcay Hayri-Olcay   4096 Aug  6 11:34 .cache
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  51304 Aug  6 11:43 fixlog20240806114001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay   1056 Aug  6 11:44 avengers.Hayri.txt
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay    324 Aug  6 11:45 fixlog20240806114555.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  49851 Aug  6 11:49 fixlog20240806114601.log
    -rw-------  1 Hayri-Olcay Hayri-Olcay   9359 Aug  6 11:59 .viminfo
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay   6573 Aug  6 12:02 newOrders.Hayri.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay 104079 Aug  6 12:03 fixlog20240806120001.log
    drwx------ 14 Hayri-Olcay Hayri-Olcay   4096 Aug  6 12:03 .config
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  50911 Aug  6 12:23 fixlog20240806122001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  50668 Aug  6 12:43 fixlog20240806124001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  49468 Aug  6 14:23 fixlog20240806142001.log
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay  49456 Aug  6 14:43 fixlog20240806144001.log
    drwxr-xr-x  5 Hayri-Olcay Hayri-Olcay   4096 Aug  6 15:38 Desktop
    -rw-rw-r--  1 Hayri-Olcay Hayri-Olcay    149 Aug  6 15:51 .gitconfig
    -rw-------  1 Hayri-Olcay Hayri-Olcay   8354 Aug  6 15:57 .bash_history
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:10 .vboxclient-clipboard-tty2-control.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:10 .vboxclient-clipboard-tty2-service.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-hostversion-tty2-control.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-seamless-tty2-control.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-draganddrop-tty2-control.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-vmsvga-session-tty2-control.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-seamless-tty2-service.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-draganddrop-tty2-service.pid
    -rw-r-----  1 Hayri-Olcay Hayri-Olcay      5 Aug  6 22:11 .vboxclient-vmsvga-session-tty2-service.pid
    drwxr-x--- 16 Hayri-Olcay Hayri-Olcay   4096 Aug  6 22:11 .
    ```

11. Run the history command:
    ```bash
    history
    ```
    _Output:_
    ```
    407  uname -a
    408  pwd
    409  cd ..
    410  pwd
    411  ls -l
    412  ls -ltr
    413  cd /
    414  pwd
    415  ls -ltr
    416  cd ~
    417  ls -ltra
    418  history
    ```
